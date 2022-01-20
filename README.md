# DHH Rails 7 Demo Reversed
This is code repository that was reversed from the original DHH Rails 7 Demo video from Youtube: <https://www.youtube.com/watch?v=mpWFrUwAN88>

## Terminal commands:

 * Setup
   * `rbenv local 2.7.5`
   * `rails _7.0.1_ new demo`
 * Chapter 1: Basic Post Model (0:00-7:00)
   * `rails generate scaffold post title:string content:text`
   * `rails db:migrate`
   * `cat db/schema.rb`
   * `rails server`
 * Chapter 2: Action Text (7:00-10:40)
   * `rails action_text:install` 
   * `bundle install`
   * `rails db:migrate`
 * Chapter 3: Import Map (10:40-13:50)
   * `./bin/importmap pin local-time`
   * `./bin/importmap pin local-time --download`
 * Chapter 4: Comments model (13:50-15:00)
   * `rails generate resource comment post:references content:text`
   * `rails db:migrate`
 * Chapter 5: Comments Action Mailer (15:00-25:00)
   * `rails g mailer comments submitted`
 * Chapter 6: Turbo streaming (25:00-27:30)
 * Chapter 7: Tests (27:30-29:30)
   * `rails test`
 * Chapter 8: Change database (29:30-30:00)
   * `rails db:system:change --to=postgresql`
   * `bundle install`
 * Chapter 9: Deploy to Heroku (30:00-34:14)
   * `git add .`
   * `bundle lock --add-platform x86_64-linux`
   * `git commit -m "First"`
   * `heroku create`
   * `git push heroku main`
   * `heroku run rake db:migrate`
   * `heroku addons:create heroku-redis:hobby-dev -a mighty-tundra-27310`
   