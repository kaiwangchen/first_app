# Ruby on Rails Tutorial: first application

This is the first application for the
[*Ruby on Rails Tutorial*](http://railstutorial.org/)
by [Michael Hartl](http://michaelhartl.com/).

http://ruby.railstutorial.org/chapters/beginning

    rvm use 2.0.0

    echo 'install: --no-rdoc --no-ri' >> ~/.gemrc
    echo 'update:  --no-rdoc --no-ri' >> ~/.gemrc
    gem install rails --version 4.0.0

    rails new first_app --skip-bundle

    cd first_app

    subl .gitignore and Gemfile
    bundle install

    rails server

    git init
    git add .
    git commit -m "Initialize repository"
    git remote add origin git@github.com:kaiwangchen/first_app.git
    git push -u origin master

    git checkout -b modify-README
    git mv README.rdoc README.md
    subl README.md
    git commit -a -m "Improve the README file"

    git checkout master
    git merge modify-README
    git branch -d modify-README
    git push


    subl Gemfile
    bundle install --without production
    git commit -a -m "Update Gemfile.lock for Heroku"

    rake assets:precompile
    git add .
    git commit -m "Add precompiled assets for Heroku"

    ...
