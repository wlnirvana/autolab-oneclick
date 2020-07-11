# Autolab OneClick Installation

1. Pull your autolab image and tag it as `autolab`
2. Pull your tango image and tag it as `tango`
3. Pull your autograding images and tag them properly
4. YOU MUST CONFIGURE TANGO PARAMETERS.
  - Copy `config.template.py` as `config.py` and search for `<TODO>`.
  - Follow Tango README.
5. YOU SHOULD CONFIGURE AUTOLAB AS WELL.
4. `cd server`
5. `docker-compose up`
6. `docker exec` into the autolab container
7. `RAILS_ENV=production bundle exec rails db:create`
8. `RAILS_ENV=production bundle exec rails db:migrate`
9. `RAILS_ENV=production bundle exec rails db:seed`
10. `chown app:app courses courseConfig assessmentConfig`
