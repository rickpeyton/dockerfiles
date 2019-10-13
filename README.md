# Dockerfiles

Collection of Dockerfiles used to build images hosted on my Docker Hub

https://cloud.docker.com/repository/docker/rickpeyton/rails

# Tag Format

ruby-#{ruby_version}-rails-#{rails_version}

i.e. `ruby-2.5.3-rails-5.2.2`

`docker build -t rickpeyton/rails:ruby-2.5.3-rails-5.2.2`

# Push

`docker push rickpeyton/rails:ruby-2.5.3-rails-5.2.2`

# Full Example

`docker build -f ruby/2.5.3/rails/5.2.2/discourse/Dockerfile -t rickpeyton/rails:ruby-2.5.3-rails-5.2.2-discourse .`

`docker push rickpeyton/rails:ruby-2.5.3-rails-5.2.2-discourse`
