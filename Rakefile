begin
  require 'echoe'
rescue LoadError
  abort "You'll need to have `echoe' installed to use Net::SSH's Rakefile"
end

require './lib/fuzzy_file_finder'
version = FuzzyFileFinder::Version::STRING.dup
if ENV['SNAPSHOT'].to_i == 1
  version << "." << Time.now.utc.strftime("%Y%m%d%H%M%S")
end

Echoe.new('fuzzy_file_finder', version) do |p|
  p.author           = "Jamis Buck"
  p.email            = "jamis@jamisbuck.org"
  p.summary          = "an implementation of TextMate's cmd-T search functionality"

  p.rdoc_pattern     = /^(lib|README.rdoc)/
end
