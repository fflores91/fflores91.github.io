# frozen_string_literal: true

source "https://rubygems.org"

# Metadata for the gemspec
gemspec

# Testing dependencies
group :test do
  gem "html-proofer", "~> 3.18"
end

# Platform-specific dependencies
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3" # Timezone library
  gem "tzinfo-data"          # Data files for Windows/JRuby
end

# Uncomment this for better file watching on Windows
# gem "wdm", "~> 0.1.1", platforms: [:mingw, :x64_mingw, :mswin]

# Compatibility for JRuby
gem "http_parser.rb", "~> 0.6.0", platforms: [:jruby]

# Specific fix for Linux-musl systems
if RUBY_PLATFORM =~ /linux-musl/
  gem "jekyll-sass-converter", "~> 2.0"
end

# Explicitly add `logger` and `csv` due to Ruby 3.4+ changes
gem "logger", "~> 1.5"
gem "csv", "~> 3.1"

# Core Jekyll dependencies
gem "jekyll", "~> 4.3.4" # Ensure the latest Jekyll version compatible with Ruby 3.2
gem "bundler", "~> 2.6"  # Lock bundler version for compatibility
