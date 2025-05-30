# Organisation

## Rails Repos

| Status (2024) | Name | Ruby version | Rails version | PG version | Frontend toolkit | javascript | deployment | host |
| ------------- | ---- | ------------ | ------------- | ---------- | ---------------- | ---------- | ---------- | ---- |
| Active | [levitate](https://github.com/Levitate-Aerospace/levitate) | 3.3.0 | 8.0.1 | 1.5.9 | | esbuild | kamal | Hetzner (~4€) |
| Active | [Systemia](https://github.com/Yoshi20/Systemia) | 3.3.0 | 7.2.1 | 1.5.7 | | esbuild | mina | Hetzner (~4.5€)* |
| Active | [Member-Card/Profile-Card/City-Deals](https://github.com/Embedded-Science/member-card) | 3.3.0 | 8.0.0 | 1.5.9 | Beercss (3.9.4) | esbuild | mina | Hetzner (~6.5€) |
| Active | [SSB-Tournament-Manager](https://github.com/Yoshi20/SSB-Tournament-Manager) | 3.1.2 | 7.1.3 | 1.1.4 | Bootstrap (4.6.2) | asset pipeline | heroku | heroku.com ($16) |
| Active | [ERUPT-IoT](https://github.com/Yoshi20/ERUPT-IoT) | 3.1.2 | 6.1.7 | 1.5.6 | Bootstrap (4.3.1) | asset pipeline | mina | Hetzner (~4€) |
| onHold | [nb-iot](https://github.com/Embedded-Science/nb-iot) | 3.3.0 | 7.1.3 | 1.5.6 | Bootstrap (5.3.3) | esbuild | mina | Hetzner (by lv) |
| onHold | [BsSApp](https://github.com/Yoshi20/bssapp) | 3.3.0 | 7.1.3 | 1.5.6 | Bootstrap (5.3.3) | esbuild | mina | Hetzner (~0€)* |
| onHold | [Beer-Button](https://github.com/Yoshi20/Beer-Button) | 3.3.0 | 7.1.3 | 1.5.5 | Beercss (3.3.5) | esbuild | mina | Hetzner (~0€)* |
| onHold | [normwert_wandler](https://github.com/Embedded-Science/normwert_wandler) | 3.1.2 | 7.1.0 | 1.5.4 | Materialize (1.0.0) | asset pipeline | mina | Hetzner (~0€)* |
| Inactive | [DeadArtists-AI](https://github.com/Yoshi20/DeadArtists-Ai) | 3.1.2 | 7.0.4 | 1.4.3 | Beercss (2.1.3) | esbuild | | |
| Inactive | [oxocare-home](https://github.com/Embedded-Science/oxocare-home) | 3.1.2 | 7.0.8 | 1.5.4 | Beercss (3.3.5) | esbuild | | |
| Inactive | [IoT-Rex](https://github.com/Yoshi20/IoT-Rex) | 2.6.5 | 6.0.1 | 1.2.3 | React (16.11.0) | asset pipeline | | |
| Inactive | [Anime-Sammlung](https://github.com/Yoshi20/Anime-Sammlung) | 2.3.0 | 4.2.4 | 0.18.4 | Bootstrap (3.3.5) | asset pipeline | | |

\* running on the same server (shared)

## Create new rails app

```
cd ~/Rails_Projects
gem update bundle && gem update --system
rails new <my_app> --database=postgresql --javascript=esbuild --css=postcss --skip-action-mailbox --skip-action-text --skip-test --skip-jbuilder
cd <my_app>
git add .
git commit -m "init"
git remote add origin git@github.com:Yoshi20/<my_app>.git
git push -u -f origin main
```

skips explained:
- action-mailbox  -> to handle incoming emails => not needed as an external service is normally used for this
- action-text     -> allows formatted text by the Trix editor on a model by impl. -> has_rich_text :content => not needed for most apps
- test            -> test files => not needed when rspec is used
- jbuilder        -> Jbuilder gives you a simple DSL for declaring JSON structures => not needed for most apps

javascript hot reload:
```
  gem 'vite_rails' # https://vite-ruby.netlify.app/

  once: bundle exec vite install
  run:  bin/vite dev
```

## Frontend Toolkits

- https://getbootstrap.com/
- https://material.io/
- https://tailwindcss.com/
- https://www.beercss.com/

## Gems Toolbox

https://www.ruby-toolbox.com/

### must have

- gem 'devise' # (flexible authentication solution)
- gem 'devise-i18n' # (devise locale data collection)
- gem 'figaro' # (ENV file: config/application.yml)
- gem 'haml-rails' # (HAML)
- gem 'honeybadger' # (health check & exception notification)
- gem 'http_accept_language' # (to detect the users preferred language)
- gem 'rails-i18n' # (rails locale data collection)

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
- gem 'mina' # (autom. deployment)

### nice to have

- gem 'aasm' # (for state maschines)
- gem 'carrierwave' (for attachments when active-storage is not sufficient) -> or gem 'paperclip'
- gem 'caxlsx' # (to generate excel data)
- gem 'caxlsx_rails'
- gem 'cookies_eu' # (to add a minimum cookie consent banner)
- gem 'jbuilder' # (for json formating)
- gem 'material_icons' # (+900 set of icons) -> or gem 'font-awesome-rails' # (font-awesome icons)
- gem 'meta-tags' # (to make your app SEO-friendly)
- gem 'newrelic_rpm' # (performance analyse in production)
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

### testing

- gem 'cucumber'
- gem 'database_cleaner'
- gem 'factory_bot'
- gem 'rspec'
- gem 'rspec_junit_formatter'
- gem 'simplecov'
- gem 'timecop'

## Hosting

### Self

1. https://www.hetzner.com/cloud

### Virtual Private Server (VPS)

1. https://www.hostinger.com/vps-hosting#slide1
2. https://www.digitalocean.com/
3. https://www.hetzner.com/webhosting/level-4

### Platform as a Service (PaaS)

1. Heroku
2. Railway App
3. EngineYard

## Health check & Monitoring

- https://app.honeybadger.io/users/sign_in
- https://www.netdata.cloud/
