# gem command extension for nexus gem repository server

* [![Build Status](https://secure.travis-ci.org/sonatype/nexus-gem.png)](http://travis-ci.org/sonatype/nexus-gem)

see
* <nexus.sonatype.org>
* <github.com/sonatype/nexus-ruby-support> for older nexus releases (before version 2.11.0)
* <github.com/sonatype/nexus-oss/plugins/rubygem> for current nexus-ruby-plugin

# installing

    gem install nexus

# usage

    gem nexus my.gem

then the command will prompt for the url, username and password. for further
info on how to deploy to more then one repo, keep the credentials file on different file system location (like on an external device) or encrypt the credentials file altogether with password based encryption:

    gem help nexus

# test, build, deploy, push #

prepare the dependencies

    bundle install
	
run tests

    bundle exec rake 
	
build and push gem to rubygems.org

    gem build nexus.gemspec
    gem push nexus-*.gem

install the gem into your local rubgems repository

    gem install -l nexus-*.gem

# contributing #

1. fork it
2. create your feature branch (`git checkout -b my-new-feature`)
3. commit your changes (`git commit -am 'Added some feature'`)
4. push to the branch (`git push origin my-new-feature`)
5. create new pull request

# meta-fu #

enjoy :) 
