source 'https://rubygems.org'

activemodel_version = ENV.fetch('ACTIVEMODEL_VERSION', '6.1')

activemodel = case activemodel_version
              when '3.2' then '3.2.22'
              when '4.0' then '4.0.13'
              when '4.1' then '4.1.16'
              when '4.2' then '4.2.11'
              when '5.0' then '5.0.7'
              when '5.1' then '5.1.7'
              when '5.2' then '5.2.3'
              when '6.0' then '6.0.0.rc1'
              end

if activemodel_version < '6.1'
  gem 'activemodel', activemodel, require: false
  gem 'activesupport', activemodel, require: false
end

group :test do
  gem 'minitest', activemodel_version < '4.1' ? '~> 4.2' : '~> 5.0'
  gem 'simplecov', require: false
end

# Specify your gem's dependencies in u-attributes.gemspec
gemspec
