# CIServerSetup

* Reference Information:
  * http://papaanton.com/setting-up-xcode-6-and-apple-server-4-0-for-continues-integration-with-cocoapods/
  * https://fastlane.tools/

## Setup Xcode Dev Machine
- brew install curl
- \curl -sSL https://get.rvm.io | bash -s stable
- rvm install ruby-head
- Install homebrew [http://brew.sh/]
  - ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
- sudo gem install nokogiri
- Install fastlane
  - https://github.com/KrauseFx/fastlane/blob/master/GUIDE.md
  - sudo gem install fastlane
  - sudo gem install fastlane_env_lanes
  - sudo gem install cert
  - sudo gem install pem
  - sudo gem install sigh
  - sudo gem install deliver
  - sudo gem install snapshot
  - sudo gem install frameit
  - sudo gem install produce

## Setup OSX Server
- Install OSX Server
- Install Xcode
- Setup OSX Server
- Follow steps above for Dev Machine

# Setup Xcode Project on Dev Machine
- cert
  - ie: ./cert TA8H33V2E6
  - ie: ./cert TA8H33V2E6 && ./sigh TA8H33V2E6 -a org.tableproject.phoenix.dev --force
- sigh
  - ie: ./sigh TA8H33V2E6 -a org.tableproject.phoenix.dev --force
  - ie: ./cert TA8H33V2E6 && ./sigh TA8H33V2E6 -a org.tableproject.phoenix.dev --force
  - sigh -a com.doublenode.dntest -u me@darrenehlers.com --adhoc
  - sigh -a com.doublenode.dntest -u me@darrenehlers.com --development
- pem
  - pem -a com.doublenode.dntest -u me@darrenehlers.com
  - pem -a com.doublenode.dntest -u me@darrenehlers.com -- development
- snapshot init
- snapshot
  - ie: snapshot --snapfile ./"Target Branding"/Phoenix-dev/Snapfile
- frameit

