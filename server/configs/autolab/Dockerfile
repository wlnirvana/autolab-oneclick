FROM autolab

COPY config/autogradeConfig.rb config/database.yml config/school.yml /home/app/webapp/config/
COPY config/environments/production.rb /home/app/webapp/config/environments/production.rb
COPY config/initializers/devise.rb /home/app/webapp/config/initializers/devise.rb
COPY nginx.conf /etc/nginx/sites-enabled/webapp.conf

RUN cd /home/app/webapp && \
  RAILS_ENV=production bundle exec rake assets:precompile && \
  mkdir -p /home/app/webapp/courses && \
  mkdir -p /home/app/webapp/courseConfig && \
  chown -R app:app /home/app/webapp
