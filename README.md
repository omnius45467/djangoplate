`Clone of http://kappataumu.com/articles/vagrant-box-django-cookiecutter-quickstart.html`
##Setting off on your own

####You can now set off on your own, by cloning the project’s repository and editing cookiestrap.sh:
```
$ git clone https://github.com/omnius45467/djangoplate.git 
$ cd vagrant-django-cookie-dough
$ vim cookiestrap.sh
$ # Edit domain_name, project_slug, db_user, db_password and cookiecutter_options
$ vagrant up
```
####As soon as the machine is brought up, browse to http://localhost:8000 to see the live website.

Inside the VM, you can find all the things in /srv/www/$domain_name/, which has been mapped locally to the www/$domain_name/ subfolder of the repository. It is in the locally mapped folder that any file editing will take place. If you’ve installed and enabled the LiveReload extension for your browser, the page will automatically be refreshed every time you edit and save a file.

Log files are kept in $domain_name/logs/, capturing the output of the Django development web server and Grunt. If anything goes wrong, you can poke around:
```
$ vagrant ssh
$ less -S +F /srv/www/$domain_name/logs/runserver.log
$ less -S +F /srv/www/$domain_name/logs/taskrunner.log
```
