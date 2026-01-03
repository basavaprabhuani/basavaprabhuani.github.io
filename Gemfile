source "https://rubygems.org"

gem "github-pages", "~> 232", group: :jekyll_plugins

group :jekyll_plugins do
  gem "jekyll-feed"
  gem "jekyll-sitemap"
end

# Windows & JRuby timezone support
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem "tzinfo", ">= 1", "< 3"
  gem "tzinfo-data"
end

# Performance booster for Windows file watching
gem "wdm", "~> 0.1", platforms: [:mingw, :x64_mingw, :mswin]
