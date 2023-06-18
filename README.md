# NationalGovernmentOrganizationHoliday

[行政機関の休日](https://elaws.e-gov.go.jp/document?lawid=363AC0000000091) を計算するgemです。

## Installation

Install the gem and add to the application's Gemfile by executing:

    $ bundle add national_government_organization_holiday

If bundler is not being used to manage dependencies, install the gem by executing:

    $ gem install national_government_organization_holiday

## Usage

```ruby
Date.new(2023, 12, 27) + 2.national_gov_org_weekdays
#=> 2024-01-04

Date.new(2023, 12, 29).on_weekday?
#=> true
value = NationalGovernmentOrganizationHoliday::Value
value.new(Date.new(2023, 12, 29)).on_weekday?
#=> false
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

`e.g. docker run -it -v $PWD/national_government_organization_holiday:/opt ruby:3.2 bash`

---

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and the created tag, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/maeda-m/national_government_organization_holiday.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
