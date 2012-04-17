# dotfiles

## Install

### Homebrew
```
sudo chown -R kamipo /usr/local
ruby -e "$(curl -fksSL https://raw.github.com/mxcl/homebrew/master/Library/Contributions/install_homebrew.rb)"

brew doctor
sudo xcode-select -switch /Applications/Xcode.app/Contents/Developer
xcode-select -print-path
```

### rbenv/ruby-build
```
brew install rbenv
brew install ruby-build

eval "$(rbenv init -)"

# ruby required libssl-dev libreadline6-dev libncurses5-dev libsqlite3-dev
# nokogiri required libxml2-dev libxslt1-dev
rbenv install 1.9.3-p125
rbenv global 1.9.3-p125
rbenv rehash
```

### perlbrew
```
curl -L http://xrl.us/perlbrewinstall | bash
source $HOME/perl5/perlbrew/etc/bashrc

perlbrew install perl-5.14.2
perlbrew install perl-5.14.2 -D=usethreads --as perl-5.14.2-usethreads
perlbrew install perl-5.14.2 -D=DEBUGGING  --as perl-5.14.2-DEBUGGING
perlbrew switch  perl-5.14.2
perlbrew install-cpanm
```

### nvm
```
git clone git://github.com/creationix/nvm.git ~/.nvm
source $HOME/.nvm/nvm.sh
nvm install v0.5.0
nvm use v0.5.0
nvm alias default v0.5.0
```

### pear
```
wget http://pear.php.net/go-pear.phar
php -d detect_unicode=0 go-pear.phar
```
