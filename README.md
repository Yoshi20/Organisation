# Organisation

## Rails Repos

| Status (2022) | Name | Ruby version | Rails version | PG version | Frontend toolkit |
| ------------- | ---- | ------------ | ------------- | ---------- | ---------------- |
| Active | SSB-Tournament-Manager | 3.1.2 | 7.0.2 | 1.1.3 | Bootstrap (4.3.1) |
| Active | ERUPT-IoT | 3.0.0 | 6.1.0 | 1.1.3 | Bootstrap (4.3.1) |
| WIP | normwert_wandler | 3.0.0 | 6.1.3 | 1.1.3 | Materialize (1.0.0) |
| Inactive | IoT-Rex | 2.6.5 | 6.0.1 | 1.2.3 | React (16.11.0) |
| Inactive | Anime-Sammlung | 2.3.0 | 4.2.4 | 0.18.4 | Bootstrap (3.3.5) |

## Gems Toolbox

### must have

- gem 'devise' # (flexible authentication solution)
- gem 'haml-rails' # (HAML)
- gem 'rails_12factor' # (Heroku integration)
- gem 'figaro' # (ENV file: config/application.yml)
- gem 'exception_notification'
- gem 'devise-i18n' # (devise locale data collection)
- gem 'rails-i18n' # (rails locale data collection)

### situational

- gem 'select2-rails' # (makes select boxes awesome)
- gem 'will_paginate' # (pagination)
- gem 'httparty' # (makes http requests fun again)
- gem 'recaptcha' # (helper methods for the reCAPTCHA API)
- gem 'acts_as_list' # (for sorting and reordering objects in a list)
- gem 'pusher-push-notifications' # (Pusher Beams using the Pusher system)
- gem 'spreadsheet' # (excel files handling)
- gem 'paper_trail' # (to track changes to your models, for auditing or versioning)
- gem 'i18n-js' # (to export translations to JavaScript)
- gem 'acts-as-taggable-on' # (to easily add tags to a model)
- gem 'twilio-ruby' (helper methods for the Twilio API)
- gem 'image_processing' # (to provides higher-level image processing helpers)
- gem 'prawn' # (fast, nimble PDF generation for ruby)
- gem 'rqrcode' # (for creating and rendering QR codes into various formats)

### nice to have

- gem 'material_icons' # (+900 set of icons based on Material Design guidelines)
- gem "font-awesome-rails" (font-awesome icons)
- gem 'http_accept_language' # (to detect the users preferred language)
- gem 'popper_js' # (for tooltips & popovers)
- gem 'meta-tags' # (to make your app SEO-friendly)
- gem 'cookies_eu' (to add a minimum cookie consent banner)
- gem 'simple_form' (allows to generate more simple forms)

### development

- gem 'pry'
- gem 'brakeman'
- gem 'rails_best_practices'
