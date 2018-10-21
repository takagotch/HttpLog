### HttpLog
---
https://github.com/trusche/httplog

https://rubygems.org/gems/httplog/versions/0.3.2

```
gem install httplog

```

```ruby
require 'httplog'

HttpLog.configure do |config|
  config.enabled = true
  config.logger = Logger.new($stdout)
  config.severity = Logger::Severity::DEBUG
  config.log_connect = true
  config.log_request = true
  config.log_headers = false
  config.log_data = true
  config.log_status = true
  conifg.log_response = true
  config.log_benchmark = true
  config.compact_log = false
  config.color = false
  config.url_whitelist_pattern = /.*/
  config.url_blacklist_pattern = nil
end

# config/environments/development.rb
HttpLog.configure do |config|
  config.logger = Rails.logger
end

HttpLog.configure do |config|
  config.color = :red
end

HttpLog.configure do |config|
  config.color = {color: :black, background: :yellow}
end

```

```
```

