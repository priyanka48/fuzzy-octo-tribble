fuzzy-octo-tribble
===================

require 'rubygems'
require 'nokogiri'
require 'open-uri'
page = Nokogiri::HTML(open("http://www.joshsoftware.com/team"))

puts page.css("title")[0].text

links = page.css("h3")
puts links.length
puts links[0].text


links.each do |i|
  puts i.text
end
