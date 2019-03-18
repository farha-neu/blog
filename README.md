# NOTES

* Creating a rails project with mysql: `rails new sample_app -d mysql`
* Generating controller and actions: `rails generate controller StaticPages home help about`
* Adding bootstrap to asset pipeline:
    1. Add `gem 'bootstrap', '~> 4.3', '>= 4.3.1'` to Gemfile
    2. `bundle install`
    3. Add `@import "bootstrap";` to app/assets/stylesheets/custom.scss
    4. Add `//= require bootstrap` in app/assets/javascripts/application.js