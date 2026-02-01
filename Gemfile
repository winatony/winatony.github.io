source "https://rubygems.org"

# Jekyll core
gem "jekyll", "~> 4.3"
gem "webrick", "~> 1.8"

# Plugins compatible with GitHub Pages
group :jekyll_plugins do
  gem "jekyll-feed", "~> 0.17"
  gem "jekyll-sitemap", "~> 1.4"
  gem "jekyll-seo-tag", "~> 2.8"
  gem "jekyll-paginate", "~> 1.1"
  gem "jemoji", "~> 0.13"
end

# Windows and JRuby timezone support
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end
