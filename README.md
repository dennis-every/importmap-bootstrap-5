# README

A demo Rails 7 app for uploading files with ActiveStorage

- Ruby 3.2.2

- Rails 7.0.4.3

- Database sqlite3

### Steps

- rails new myapp
- Add gem bootstrap
- Add gem sassc-rails
- Add @import "bootstrap" to app/assets/stylesheets/application.scss
- Optionally you might need to run bin/rails assets:precompile to generate the css

### To add Bootstrap js

#### Precompile the bootstrap.min.js that comes with the gem, by adding to config/initializers/assets.rb:

- Rails.application.config.assets.precompile += %w( bootstrap.min.js popper.js )

#### Pin the compiled asset in config/importmap.rb:

- pin "popper", to: 'popper.js', preload: true
- pin "bootstrap", to: 'bootstrap.min.js', preload: true

#### Include bootstrap in your app/javascript/application.js:

- import "popper"
- import "bootstrap"
- Optionally you might need to run bin/rails assets:precompile to generate the js

### Test that Bootstrap js is working

- Add [modal example](https://getbootstrap.com/docs/5.2/components/modal/#live-demo)
