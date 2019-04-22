# NOTES

* Creating a rails project with mysql: `rails new sample_app -d mysql`
* Generating controller and actions: `rails generate controller StaticPages home help about`
* Adding bootstrap to asset pipeline:
    1. Add `gem 'bootstrap', '~> 4.3', '>= 4.3.1'` to Gemfile
    2. `bundle install`
    3. Add `@import "bootstrap";` to app/assets/stylesheets/custom.scss
    4. Add `//= require bootstrap` in app/assets/javascripts/application.js
* Creating record in database:
    1. Create a model: `rails generate controller Users new`
    2. `rails generate model User name:string email:string`
    3. `rails db:migrate`
* Saving a record to DB:
    1. Option 1: `user = User.new(name: 'Farha', email:'farhajw@gmail.com')`  
                  `user.save`
    2. Option 2: `User.create(name: 'Farha', email:'farhajw@gmail.com')`

* Destroying a record from DB:
     `user.destroy`

* Finding a record:
    1. User.find(1)
    2. User.find_by(email:"example@example.com")
    3. User.first
    4. User.all -> returns an array of users

* Updating a record:
    1. Option 1: `user.email = "my@my.com"`  
                  `user.save`
    2. Option 2: `user.update_attributes(name:"Farha")`
 
 * Generating a migration:
   `rails generate migration add_remember_digest_to_users remember_digest:string`

* Content Tag:
    `<%= content_tag(:div,"Hello", class:"alert alert-danger") %>`

* Paginate: `User.paginate(page:1)` => 30 users by default per page
    
* Mailer generation: `rails generate mailer UserMailer account_activation password_reset`
* `rails generate model Micropost content:text user:references`