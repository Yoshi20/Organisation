# Organisation

## Rails Repos

| Status (2022) | Name | Ruby version | Rails version | PG version | Frontend toolkit | javascript | host |
| ------------- | ---- | ------------ | ------------- | ---------- | ---------------- | ---------- | ---- |
| WIP | [DeadArtists-AI](https://github.com/Yoshi20/DeadArtists-Ai) | 3.1.2 | 7.0.3 | 1.4.3 | Beercss (2.1.3) | esbuild | railway.app |
| WIP | [oxocare-home](https://github.com/Embedded-Science/oxocare-home) | 3.1.2 | 7.0.3 | 1.4.2 | Beercss (2.1.3) | esbuild | |
| Active | [SSB-Tournament-Manager](https://github.com/Yoshi20/SSB-Tournament-Manager) | 3.1.2 | 7.0.2 | 1.1.3 | Bootstrap (4.3.1) | asset pipeline | heroku.com |
| Active | [ERUPT-IoT](https://github.com/Yoshi20/ERUPT-IoT) | 3.0.0 | 6.1.0 | 1.1.3 | Bootstrap (4.3.1) | asset pipeline | heroku.com |
| WIP | [normwert_wandler](https://github.com/Embedded-Science/normwert_wandler) | 3.0.0 | 6.1.3 | 1.1.3 | Materialize (1.0.0) | asset pipeline | heroku.com |
| Inactive | [IoT-Rex](https://github.com/Yoshi20/IoT-Rex) | 2.6.5 | 6.0.1 | 1.2.3 | React (16.11.0) | asset pipeline | |
| Inactive | [Anime-Sammlung](https://github.com/Yoshi20/Anime-Sammlung) | 2.3.0 | 4.2.4 | 0.18.4 | Bootstrap (3.3.5) | asset pipeline | |

## Create new rails app

```
cd ~/Rails_Projects
gem update bundle && gem update --system
rails new <my_app> --database=postgresql --javascript=esbuild --css=sass
```

## Frontend Toolkits

- https://getbootstrap.com/
- https://material.io/
- https://tailwindcss.com/
- https://www.beercss.com/

## Gems Toolbox

### must have

- gem 'devise' # (flexible authentication solution)
- gem 'devise-i18n' # (devise locale data collection)
- gem 'exception_notification'
- gem 'figaro' # (ENV file: config/application.yml)
- gem 'haml-rails' # (HAML)
- gem 'http_accept_language' # (to detect the users preferred language)
- gem 'rails-i18n' # (rails locale data collection)
- gem 'rails_12factor' # (Heroku integration)
- gem 'sassc-rails' # (Use Sass to process CSS) -> or use sass-rails instead

### situational must have

- gem 'acts_as_list' # (for sorting and reordering objects in a list)
- gem 'acts-as-taggable-on' # (to easily add tags to a model)
- gem 'httparty' # (makes http requests fun again)
- gem 'i18n-js' # (to export translations to JavaScript)
- gem 'image_processing' # (to provide higher-level image processing helpers)
- gem 'paper_trail' # (to track changes to your models, for auditing or versioning)
- gem 'prawn' # (fast, nimble PDF generation for ruby) -> or gem 'pdfkit' or gem 'wickedpdf'
- gem 'pusher-push-notifications' # (Pusher Beams using the Pusher system)
- gem 'recaptcha' # (helper methods for the reCAPTCHA API)
- gem 'rqrcode' # (for creating and rendering QR codes into various formats)
- gem 'select2-rails' # (makes select boxes awesome) -> or use https://tom-select.js.org/ instead (to not use jQuery)
- gem 'spreadsheet' # (excel files handling)
- gem 'twilio-ruby' (helper methods for the Twilio API)
- gem 'will_paginate' # (pagination)

### nice to have

- gem 'aasm' # (for state maschines)
- gem 'carrierwave' (for attachments when active-storage is not sufficient) -> or gem 'paperclip'
- gem 'caxlsx' # (to generate excel data)
- gem 'caxlsx_rails'
- gem 'cookies_eu' # (to add a minimum cookie consent banner)
- gem 'jbuilder' # (for json formating)
- gem 'material_icons' # (+900 set of icons) -> or gem 'font-awesome-rails' # (font-awesome icons)
- gem 'meta-tags' # (to make your app SEO-friendly)
- gem 'newrelic_rpm' # (performance analyse in prdouction)
- gem 'pluck_to_hash' # (.pluck directly as hash instead of array)
- gem 'popper_js' # (for tooltips & popovers)
- gem 'rollbar' # (error handling) -> or gem 'honeybadger'
- gem 'ruby-progressbar' # (progressbar for rake tasks)
- gem 'simple_form' (allows to generate more simple forms)

### development

- gem 'better_errors'
- gem 'brakeman'
- gem 'bullet' # (DB Query und Index Analyse)
- gem 'pry'
- gem 'pry-rails' # (pry automatisch laden)
- gem 'rack-mini-profiler' # (Performance Analyse)
- gem 'rails_best_practices'

### testing

- gem 'cucumber'
- gem 'database_cleaner'
- gem 'factory_bot'
- gem 'rspec'
- gem 'rspec_junit_formatter'
- gem 'simplecov'
- gem 'timecop'
