Minimal repo to demonstrate bundler / rbenv / guard [issue](https://github.com/bundler/bundler/issues/4592)

Tested locally on:

* arch-linux (rolling release updated 2016-05-23)
* bundler 1.12.4
* rbenv 1.0.0
* ruby 2.3.1p112 (2016-04-26 revision 54768) [x86_64-linux]

(also tested on ruby versions: 2.0.0-p247, 2.1.9, 2.2.5, 2.3.1)

Using vendored bundle path: `bundle install --path vendor`

bundle exec guard - [output](gists/bundle_exec_guard)

bundle env - [output](gists/bundle_env)

gem env - [output](gists/gem_env)

## Working variants tested

1. bundle without using vendored path (works with all 1.12.x versions of bundler tested below)
2. bundler < `1.12.0.pre.2`
3. bundler <= `3f5e0181` (before PR 4298)

## Non-working variants tested

bundle using vendored path on following versions of bundler

* bundler: `6678cd73`, 1.12.0.pre.2, 1.12.4
