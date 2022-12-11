# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## Instructions

1. Run the following to scaffold this project: `rails new ruby-on-rails-graph-blog -T -d postgresql`

2. Install the GraphQL gem found on [rubgems.org](https://rubygems.org/gems/graphql/versions/2.0.15). Find the "Gemfile" code segment `gem 'graphql', '~> 2.0', '>= 2.0.15'` and copy it to the bottom of your Gemfile. Then run `bundle install` in the top-level directory

3. Afterwards take a look at the documentation. You will need to run `rails generate graphql:install`. This command will do a few things:

- Generate a folder structure
- Add a bunch of definitions such as GraphQL schema type definition, query type definition, mutation type definition
- Routing and controller for executing queries

4. You will find another gem that has been added to the Gemfile. `gem "graphiql-rails", group: :development`. So you must run `bundle install` before continuing to create your models.

5. Generate your models; for the user, `rails generate model User first_name last_name address postcode city country`; for the posts, `rails g model Post user:references body`; and for comments, `rails g model COmment user:references post:references body`. Then run `rails db:create db:migrate`
