### knock
---

https://github.com/nsarno/knock

```
gem 'knock'
bundle install
rails g knock:install
rails g knock:token_controller user

class User < ActiveRecord::Base
  has_secure_password
end

class ApplicationController < ActionController::API
  include Knock::Authenticable
end

class SecuredController < ApplicationController
  before_action :authenticate_user
  
  def index
  end
end


...








```
.py
