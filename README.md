<p align="center">
<img src="https://github.com/minio/doctor/blob/master/public/Doctor_logo_888x1024.png?raw=true" width="140px">
</p>

# What is Doctor
* Doctor is a Documentation Server for all your project docs.
* Doctor beautifully decouples document serving and document contents.
* Create your docs in markdown. Store them anywhere (github/dropbox/google drive/ anywhere really).
* Login to Doctor's Dashboard. Setup links to your doc files in Doctor's Dashboard.
* You are done!

## Live Demo
* [Doctor's website](http://getdoctor.io) is a site hosted on doctor using this very Readme.MD file. Yeah very meta.
* [Minio Docs](https://docs.minio.io) has a doctor server running that pulls together MD files that reside across a number of github repos :
 Eg: 
  * README.md in https://github.com/minio/minio
  * Markdown files in https://github.com/minio/minio/tree/master/docs
  
You may use the `Suggest Edits` feature in Doctor to submit changes to any of the MD files in github. Doctor relies on github workflow to accept PRs for changes. 

## Deployment

### Heroku
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/minio/doctor)

### Scalingo
[![Deploy](https://cdn.scalingo.com/deploy/button.svg)](https://my.scalingo.com/deploy?source=https://github.com/minio/doctor)

### Docker
[![Doctor.Docker](https://d207aa93qlcgug.cloudfront.net/1.95.5.qa/img/nav/docker-logo-loggedout.png)](https://hub.docker.com/r/minio/doctor/)

```
docker pull minio/doctor
```
#### Using Docker Pull

```bash
> git clone https://github.com/minio/doctor.git
> cd doctor
> docker-compose up
```

## Features
* Documents are organized under Categories.
* Login to the dashboard
* Step 1 : Use the Dashboard to create a new Category : http://localhost:3000/categories/new
* Step 2 : Use the Dashboard to create a link to a new Document : http://localhost:3000/docs/new
* Step 3: Paste the raw URL to the md file when linking a new document. The "Raw" button is on the top of the MD file in github.
* Required : All documents need to be associated under a Category

## Development 

### Quickstart: Setup on OSX
* Install Ruby 2.2.2 using the instructions [here](https://rvm.io/rvm/install).
* Install Rails 4.2.4 using the instructions [here](https://rvm.io/rvm/install).
* Install Postgres using the command `brew install postgres`. Configure Launch Agent to start it automatically or use the command `pg_ctl -D /usr/local/var/postgres -l /usr/local/var/postgres/server.log start` to start it manually.

### Quickstart: Setup on Ubuntu
* Install Rails & Ruby using the instructions [here](https://www.digitalocean.com/community/tutorials/how-to-install-ruby-on-rails-on-ubuntu-14-04-using-rvm).
* Install Postgres using the instructions [here](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04).

Clone and start doctor

```
> git clone https://github.com/minio/doctor.git
> cd doctor
> bundle install
> rake db:drop
> rake db:setup
> rails s
```
Now visit http://localhost:3000

Use `sysadmin@doctor.io` with password `Doctor!23` to login. Visit [http://localhost:3000](http://localhost:3000) to navigate the docs. This can be changed anytime via the Dashboard. We highly recommend that you do if you use Doctor in deployment.

**Note** - Ping us on our [gitter channel](https://gitter.im/minio/minio) to report any installation issues on your platform.

