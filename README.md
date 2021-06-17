This repo is a minimal reproduction of https://github.com/rubygems/rubygems/issues/4338

To create the issue, do the following:

1. Make sure you are using ruby 3.0.1
2. `bundle install`
3. `rake install --trace` (should produce error: "Couldn't install gem, run `gem install <path>' for more detailed output")
4. `gem install --backtrace <path>` using the path from the error in previous step (should produce error: `undefined method `request' for nil:NilClass`)
