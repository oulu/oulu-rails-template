Rails template for oulu. 

## Gemfile

    # View tools
    gem 'browser'
    gem 'respond-rails'

    # Sass
    gem 'modular-scale'
    gem 'sass-rails', git: 'git://github.com/machida/sass-rails.git', branch: 'sass3'
    gem 'compass', '~> 1.0.0.alpha.19'
    gem 'compass-rails', '~> 1.1.7'
    # gem 'oulu-rails', path: '../oulu-rails'
    gem 'oulu-rails', '~> 0.3.11', github: 'oulu/oulu-rails'

    # Dev tools
    group :development do
      gem 'quiet_assets'
      gem 'xray-rails'
    end
    
## application.rb

Add to `class Application < Rails::Application`.

    # Use oulu
    config.compass.require 'rgbapng'
    config.compass.require 'SassyLists'
    config.compass.require 'ceaser-easing'
 
## application.css.sass

    //////////////
    // settings
    //////////////

    // oulu variables
    // copy from https://github.com/oulu/oulu-rails/blob/master/vendor/assets/stylesheets/settings/variables/_default.css.sass
    @import settings/variables/oulu    


    // oulu
    @import oulu

    // oulu-options
    @import options/web-fonts/font-awsome
    @import options/web-fonts/lato
    @import options/web-fonts/open-sans
    @import options/web-fonts/montserrat
    …
 
## application.js

    //= require oulu