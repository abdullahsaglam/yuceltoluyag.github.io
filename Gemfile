source 'https://rubygems.org'

gem "jekyll", "~> 4.2.0"
gem "bundler"

group :jekyll_plugins do
  gem "jekyll-sitemap"
  gem "jekyll-seo-tag"
  gem "jekyll-feed"
  gem "jekyll-paginate"
  gem "jekyll-mentions"
  gem "jekyll-redirect-from"
  gem "jemoji"
  gem "sprockets"
  gem "mini_magick"
  gem "jekyll-octicons"
end

# Development Gems
group :development do
    gem "html-proofer"
    gem "fileutils"
    gem "thin"
    gem "rack"
    gem "webrick", "~> 1.7"
end
# Windows and JRuby does not include zoneinfo files, so bundle the tzinfo-data gem
# and associated library.
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", "~> 1.2"
  gem "tzinfo-data"
end

# Performance-booster for watching directories on Windows
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]

