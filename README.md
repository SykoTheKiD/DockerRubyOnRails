## Ruby on Rails Application in Docker with Continuous Integration
### Includes
* Ruby + Rails
* Puma
* Travis CI Integration

### Setup
1. Place the entire contents of your Rails project inside the `app/` folder
2. Inside your **Gemfile** add the **puma** gem. (`gem 'puma'`)
3. Add the `puma.rb` file inside the `config` folder of your Rails project

### Docker Deployment
1. Run `docker-compose build`
2. After building run `docker-compose up` to start up the Puma Server
3. In your browser go to your docker machine's IP address on port 3000 and you should see your app running
