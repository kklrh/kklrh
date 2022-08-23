Worker information
0.19s0.00s0.01s0.00s0.01s
system_info
Build system information
0.01s0.01s0.67s0.35s0.07s0.00s0.06s0.00s0.01s0.01s0.01s0.01s0.01s0.00s0.00s0.03s0.00s0.01s0.35s0.00s0.00s0.00s0.01s0.00s0.12s0.01s1.16s0.00s0.11s6.04s0.00s4.39s0.00s2.80s
docker_mtu_and_registry_mirrors
resolvconf
install_chrome
$ export CHROME_SOURCE_URL=https://dl.google.com/dl/linux/direct/google-chrome-stable_current_amd64.deb
git.checkout
2.65s$ git clone --depth=50 https://github.com/travis-ci/travis-web.git travis-ci/travis-web
0.02s
Setting environment variables from repository settings
$ export encrypted_0a9876yjhgvbnhy98765=[secure]
$ export SAUCE_USERNAME=travisci
$ export SAUCE_ACCESS_KEY=[secure]
$ export SEGMENT_STAGING_KEY=[secure]
$ export PERCY_TOKEN=[secure]
$ export PERCY_PROJECT=travis-ci/travis-web
$ export GH_TOKEN=[secure]
$ export QUAY_ROBOT_HANDLE=[secure]
$ export QUAY_ROBOT_TOKEN=[secure]
$ export AWS_KEY=[secure]
$ export AWS_SECRET=[secure]
$ export GITHUB_TOKEN=[secure]
$ export HEROKU_API_KEY=[secure]
$ export STRIPE_PUBLISHABLE_KEY=[secure]
$ export FLAG_GITLAB_LOGIN=true
$ export GITHUB_ORGS_OAUTH_ACCESS_SETTINGS_URL=[secure]
$ export REDIS_URL=[secure]
$ export FLAG_ENABLE_BITBUCKET_LOGIN=true
$ export ORG_PRODUCTION_REDIS_URL=[secure]
$ export COM_PRODUCTION_REDIS_URL=[secure]
Setting environment variables from .travis.yml
$ export PATH=/snap/bin:$PATH
$ export PERCY_ENABLE=0
$ export JOBS=1
nvm.install
142.89s$ nvm install 10
cache.1
Setting up build cache
cache.npm
$ node --version
v10.24.1
$ npm --version
6.14.12
$ nvm --version
0.39.1
before_install.1
0.24s$ npm config set spin false
before_install.2
1.35s$ npm install -g greenkeeper-lockfile@1
install
397.44s$ npm ci
before_script.1
0.01s$ if [ $TRAVIS_PULL_REQUEST = 'false' ] && [ $TRAVIS_EVENT_TYPE != 'cron' ]; then echo "Enabling Percy on push with default Ember" && export PERCY_ENABLE=1; else export PERCY_ENABLE=0; fi
before_script.2
0.00s$ echo $PERCY_ENABLE
before_script.3
0.00s$ if [ "$PERCY_ENABLE" -ne 1 ]; then export RANDOMISE=--random; fi
before_script.4
0.00s$ echo $RANDOMISE
before_script.5
0.11s$ greenkeeper-lockfile-update
13.95s$ if [ -z "$TRY_CONFIG" ]; then npm run lint:js; fi
> travis@0.0.1 lint:js /home/travis/build/travis-ci/travis-web
> eslint .
The command "if [ -z "$TRY_CONFIG" ]; then npm run lint:js; fi" exited with 0.
246.45s$ if [ -z "$TRY_CONFIG" ]; then ember exam --reporter dot $RANDOMISE; fi
[ember-cli-dotenv]: ENOENT: no such file or directory, open '/home/travis/build/travis-ci/travis-web/.env'
Browserslist: caniuse-lite is outdated. Please run next command `npm update`
Could not start watchman
Visit https://ember-cli.com/user-guide/#watchman for more info.
Randomizing tests with seed: dhdz7isdb4l
Building
[ember-cli-dotenv]: ENOENT: no such file or directory, open '/home/travis/build/travis-ci/travis-web/.env'
WARNING: [ember-cli-dotenv]: Required environment variable 'API_ENDPOINT' is missing.
WARNING: [ember-cli-dotenv]: Required environment variable 'TRAVIS_PRO' is missing.
WARNING: [ember-cli-dotenv]: Required environment variable 'ENABLE_FEATURE_FLAGS' is missing.
Environment: test
Browserslist: caniuse-lite is outdated. Please run:
npx browserslist@latest --update-db
Why you should do it regularly:
https://github.com/browserslist/browserslist#browsers-data-updating
Browserslist: caniuse-lite is outdated. Please run:
npx browserslist@latest --update-db
Why you should do it regularly:
https://github.com/browserslist/browserslist#browsers-data-updating
Browserslist: caniuse-lite is outdated. Please run:
npx browserslist@latest --update-db
cleaning up
cleaning up...
Built project successfully. Stored in "/home/travis/build/travis-ci/travis-web/tmp/class-tests_dist-jOx5zkew.tmp".
  WARNING: [ember-cli-dotenv]: Required environment variable 'API_ENDPOINT' is missing.
WARNING: [ember-cli-dotenv]: Required environment variable 'TRAVIS_PRO' is missing.
WARNING: [ember-cli-dotenv]: Required environment variable 'ENABLE_FEATURE_FLAGS' is missing.
................................*............................
  ..........*..................................................
  .........*.....................*.............................
  .............................................................
  ...........*.................................................
  .............................................................
  .............................................................
  .............................................................
  .............................................................
  ............*............................*...................
  ...................................*...................*.....
  .............................................................
  .....................................................**......
  ..*..........................................................
  .............................................................
  .............................................................
  .............................................................
  .............................................................
  .............................................................
  .............................................................
  ........*.........*..........................................
  .............................................................
  .........................................................*...
  .*...........................................................
  ...
  1467 tests complete (131908 ms)
The command "if [ -z "$TRY_CONFIG" ]; then ember exam --reporter dot $RANDOMISE; fi" exited with 0.
0.01s$ if [[ ! -z "$TRY_CONFIG" ]]; then ember try:one $TRY_CONFIG --skip-cleanup; fi
The command "if [[ ! -z "$TRY_CONFIG" ]]; then ember try:one $TRY_CONFIG --skip-cleanup; fi" exited with 0.
cache.2
store build cache
after_script.1
0.11s$ greenkeeper-lockfile-upload
after_script.2
260.19s$ test $TRAVIS_PULL_REQUEST && test $TRAVIS_PULL_REQUEST != 'false' && $TRAVIS_SECURE_ENV_VARS == 'true' && ./config/deployment/deploy-pull-request.sh
Done. Your build exited with 0.
