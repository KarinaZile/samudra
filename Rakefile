# frozen_string_literal: true

require "pry-byebug"
require 'wicked_pdf'

# To use the PDF generator, run:
#
# bundle exec rake "generate_pdf[my-page]"
#
# where my-page is the name of the page you want to generate a PDF for, eg:
# https://www.samudra.world/my-page
#
# The page must be in the _site directory.
# The PDF will be generated in the _site directory.
#
# To add a page break in the PDF, add the following to the page:
#
# <div class="page-break"></div>
desc "Generate a PDF from a HTML file"
task :generate_pdf, [:page] do |_task, args|
  name = args[:page]
  html_file = "_site/#{name}/index.html"
  html = File.read(html_file)

  # Strip out the footer
  html.gsub!(/<footer.*footer>/m, "")

  # Remove the div with the id attribute "navigation"
  html.gsub!(/<div id="navigation".*#navigation -->/m, "")

  # Add a localhost domain to all src and href attributes
  html.gsub!(/(src|href)="\/(.*?)"/, '\1="http://localhost:4000/\2"')

  # Remove the <figure> large image as it makes text unreadable
  html.gsub!(/<figure.*figure>/m, "")

  # Add styles to allow page breaks
  line_break_css = <<~HTML
    <style media="screen,print">
    .page-break {
      page-break-before: always !important;
    }
    /* https://github.com/wkhtmltopdf/wkhtmltopdf/issues/2982#issuecomment-416950855 */
    .columns.end {
      float: none;
    }
    </style>
  HTML
  html.gsub!("</head>", "#{line_break_css}</head>")

  print_from = "#{html_file}-print.html"
  File.write(print_from, html)

  # Use advanced PDF features here
  # See https://github.com/mileszs/wicked_pdf#advanced-usage-with-all-available-options
  pdf = WickedPdf.new.pdf_from_string(
    File.read(print_from),
    margin: {
      top: 20, # default 10 (mm)
      bottom: 20,
      left: 20,
      right: 20
    },
    zoom: 1.3,
  )

  # then save to a file
  pdf_file = "#{html_file}.pdf"
  File.open(pdf_file, 'wb') do |file|
    file << pdf
  end

  puts "PDF generated: #{pdf_file}"

  exit 1
end
