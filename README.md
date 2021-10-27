# Developers Mac

> An awesome project.


## Customizing System Preferences

### Trackpad Options

- Go To `System Preferences > Trackpad`.
- Enable all options across all tabs.
- Back & go to `System Preferences > Accessibility > Mouse & Trackpad > Trackpad Options`.
- Enable dragging with `three finger drag`.

### Date & Time Options

- Go To `System Preferences > Date & Time > Clock`.
- Uncheck `Use a 24-hour clock`.
- Check `Show date`.
- Check `Announce the time` `On the hour`.

### Sound Options
- Go To `System Preferences > Sound`.
- Check `Show volume in menu bar`.

### Bluetooth Options
- Go To `System Preferences > Bluetooth`.
- Check `Show Bluetooth in menu bar`.

### User Options
- Go To `System Preferences > User & Groups`.
- Disable `Guest User Login`.

### Security & Privacy Options

- Go To `System Preferences > Security & Privacy`.
- Change `Require password` value to `immediately`.
- Turn on `Filevault`. I already on it during Mac setup.
- Turn on `Firewall`.

### Dock Options

- Go To `System Preferences > Dock`.
- Check all checkboxes except `Magnification`.

## Finder Options

- Go To `Finder Preferences > Sidebar`.
- Check home directory.
- On `Advanced` tab select `Search The Current Folder` for `When Performing a Search`.
- `Finder > View > Show Tab Bar, Show Status Bar, Show Path Bar`.
- `Finder > View > Show View Options > Calculate All Size > Use as Defaults`.

## Terminal Preferences

- Go To `Terminal Preferences`.
- On startup, open new window with `Pro`.
- New windows open with `Same Profile`.

## Install Applications From AppStore
- [Xcode](https://itunes.apple.com/us/app/xcode/id497799835)
- [The Unarchiver](https://itunes.apple.com/us/app/the-unarchiver/id425424353) 
- [Microsoft Remote Desktop] 10(https://itunes.apple.com/us/app/slack/id803453959)
- [Slack](https://itunes.apple.com/us/app/slack/id803453959)
- [Guidance](https://itunes.apple.com/us/app/guidance/id412759995)

## Install 3rd Party Applications

- [LastPass](https://lastpass.com/misc_download2.php?tab=windows&anchor=sfjsarif
- )
- [Google Chrome](https://www.google.com/chrome/?brand=CHBD&gclid=EAIaIQobChMI3eyx29Pf3gIVXAQqCh3NYQo2EAAYASABEgJg4_D_BwE&gclsrc=aw.ds)
- [Firefox Developer Edition](https://www.mozilla.org/en-US/firefox/developer/)
- [Chatwork](https://go.chatwork.com/download/)
- [Skype](https://www.skype.com/en/)
- [PHPStorm](https://www.jetbrains.com/phpstorm/)
- [Sequel Pro](https://sequelpro.com/test-builds)
- [LibreOffice](https://www.libreoffice.org/download/download/)
- [CleanMyMac X]()
- [FileZilla](https://filezilla-project.org/download.php?type=client)
- [SourceTree](https://www.sourcetreeapp.com)
- [Fork](https://git-fork.com)
- [Shuttle](http://fitztrev.github.io/shuttle/)
- [Dropbox](https://www.dropbox.com/install)
- [Avro](https://www.omicronlab.com/iavro.html)

## Copy All Backup Files

- `~/.bash_profile`
- `~/.gitignore_global`
- `~/.gitconfig`
- `~/.ssh`

## Dev Environment Setup
### Git Config
### Install [Composer](https://getcomposer.org/download/)

```
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '93b54496392c062774670ac18b134c3b3a95e5a5e5c8f1a9f115f203b75bf9a129d5daa8ba6a13e2cc8a1da0806388a8') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mkdir -p /usr/local/bin
sudo mv composer.phar /usr/local/bin/composer
```
### Install [Homebrew](https://brew.sh)

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install [Valet](https://laravel.com/docs/5.7/valet)

```
brew install php
brew install mysql@5.7
brew link mysql@5.7 --force
composer global  require laravel/valet
valet install
cd ~/Sites
valet park
```

### MySQL Configuration

```
Biplobs-MacBook-Pro:Sites biplob$ brew services restart mysql@5.7

==>  Successfully started `mysql@5.7` (label: homebrew.mxcl.mysql@5.7)

Biplobs-MacBook-Pro:Sites biplob$ mysql_secure_installation

  

Securing the MySQL server deployment.

  

Connecting to MySQL using a blank password.

  

VALIDATE PASSWORD PLUGIN can be used to test passwords

and improve security. It checks the strength of password

and allows the users to set only those passwords which are

secure enough. Would you like to setup VALIDATE PASSWORD plugin?

  

Press y|Y for Yes, any other key for No: n

Please set the password for root here.

  

New password:

  

Re-enter new password:

By default, a MySQL installation has an anonymous user,

allowing anyone to log into MySQL without having to have

a user account created for them. This is intended only for

testing, and to make the installation go a bit smoother.

You should remove them before moving into a production

environment.

  

Remove anonymous users? (Press y|Y for Yes, any other key for No) : y

Success.

  

  

Normally, root should only be allowed to connect from

'localhost'. This ensures that someone cannot guess at

the root password from the network.

  

Disallow root login remotely? (Press y|Y for Yes, any other key for No) : y

Success.

  

By default, MySQL comes with a database named 'test' that

anyone can access. This is also intended only for testing,

and should be removed before moving into a production

environment.

  

  

Remove test database and access to it? (Press y|Y for Yes, any other key for No) : y

- Dropping test database...

Success.

  

- Removing privileges on test database...

Success.

  

Reloading the privilege tables will ensure that all changes

made so far will take effect immediately.

  

Reload privilege tables now? (Press y|Y for Yes, any other key for No) : y

Success.

  

All done!
```

### Install & Configure [xDebug](https://xdebug.org/docs/install) with PHPStorm

- Open PHPStorm Preferences (Cmd +,)
- Search with xDebug
- Follow the steps.

```
pecl install xdebug
```

### Install Blackfire

- Follow these steps https://blackfire.io/docs/up-and-running/installation

### Download & Setup my Config Repo
### Bash Profile
### Install [PHP-CS-Fixer](https://cs.sensiolabs.org/)

```
composer global require friendsofphp/php-cs-fixer
```

[Configure PHPStorm to use PHP-CS-Fixer](https://hackernoon.com/how-to-configure-phpstorm-to-use-php-cs-fixer-1844991e521f)

### Install Deployer

- Follow the steps on https://c5japaninc.backlog.jp/git/COMPANY/deployer/tree/master


### Install [PHPUnit](https://phpunit.readthedocs.io/en/7.4/installation.html)

```
wget https://phar.phpunit.de/phpunit.phar
chmod +x phpunit.phar 
sudo mv phpunit.phar /usr/local/bin/phpunit
phpunit --version
```