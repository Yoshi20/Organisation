# Organisation

## Rails Repos

| Status (2022) | Name | Ruby version | Rails version | PG version | Frontend toolkit | javascript |
| ------------- | ---- | ------------ | ------------- | ---------- | ---------------- | ---------- |
| WIP | oxocare-home | 3.1.2 | 7.0.3 | 1.1.? | Beercss (2.2.1) | esbuild |
| Active | SSB-Tournament-Manager | 3.1.2 | 7.0.2 | 1.1.3 | Bootstrap (4.3.1) | asset pipeline |
| Active | ERUPT-IoT | 3.0.0 | 6.1.0 | 1.1.3 | Bootstrap (4.3.1) | asset pipeline |
| WIP | normwert_wandler | 3.0.0 | 6.1.3 | 1.1.3 | Materialize (1.0.0) | asset pipeline |
| Inactive | IoT-Rex | 2.6.5 | 6.0.1 | 1.2.3 | React (16.11.0) | asset pipeline |
| Inactive | Anime-Sammlung | 2.3.0 | 4.2.4 | 0.18.4 | Bootstrap (3.3.5) | asset pipeline |

## Create new rails app

rails new <my_app> --database=postgresql --javascript=esbuild

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

### situational

- gem 'acts_as_list' # (for sorting and reordering objects in a list)
- gem 'acts-as-taggable-on' # (to easily add tags to a model)
- gem 'httparty' # (makes http requests fun again)
- gem 'i18n-js' # (to export translations to JavaScript)
- gem 'image_processing' # (to provides higher-level image processing helpers)
- gem 'paper_trail' # (to track changes to your models, for auditing or versioning)
- gem 'prawn' # (fast, nimble PDF generation for ruby)
- gem 'pusher-push-notifications' # (Pusher Beams using the Pusher system)
- gem 'recaptcha' # (helper methods for the reCAPTCHA API)
- gem 'rqrcode' # (for creating and rendering QR codes into various formats)
- gem 'select2-rails' # (makes select boxes awesome)
- gem 'spreadsheet' # (excel files handling)
- gem 'twilio-ruby' (helper methods for the Twilio API)
- gem 'will_paginate' # (pagination)

### nice to have

- gem 'cookies_eu' (to add a minimum cookie consent banner)
- gem "font-awesome-rails" (font-awesome icons)
- gem 'material_icons' # (+900 set of icons based on Material Design guidelines)
- gem 'meta-tags' # (to make your app SEO-friendly)
- gem 'popper_js' # (for tooltips & popovers)
- gem 'simple_form' (allows to generate more simple forms)

### development

- gem 'brakeman'
- gem 'pry'
- gem 'rails_best_practices'
