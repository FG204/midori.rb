# midori

**This project is still not production-ready. Questions, suggestions and pull requests are highly welcome.**

![Logo and Slogan](https://github.com/midori-rb/midori.rb/raw/master/.resources/slogan.png)

## Description

Midori is a Ruby Web Framework, providing high performance and proper abstraction.

|                  midori                  | [midori-contrib](https://github.com/midori-rb/midori-contrib) | [murasaki](https://github.com/midori-rb/murasaki) | [midori_http_parser](https://github.com/midori-rb/http_parser.rb) |
| :--------------------------------------: | :--------------------------------------: | :--------------------------------------: | :--------------------------------------: |
| ![midori logo](https://github.com/midori-rb/midori.rb/raw/master/.resources/midori_logo.png) | ![midori logo](https://github.com/midori-rb/midori.rb/raw/master/.resources/contrib_logo.png) | ![midori logo](https://github.com/midori-rb/midori.rb/raw/master/.resources/murasaki_logo.png) | ![midori logo](https://github.com/midori-rb/midori.rb/raw/master/.resources/parser_logo.png) |
|              Web Framework               |           Official Extensions            |         Modularized Event Engine         |               HTTP Parser                |
| [![Build Status](https://travis-ci.org/midori-rb/midori.rb.svg?branch=master)](https://travis-ci.org/midori-rb/midori.rb) | [![Build Status](https://travis-ci.org/midori-rb/midori-contrib.svg?branch=master)](https://travis-ci.org/midori-rb/midori-contrib) | [![Build Status](https://travis-ci.org/midori-rb/murasaki.svg?branch=master)](https://travis-ci.org/midori-rb/murasaki) | [![Build Status](https://travis-ci.org/midori-rb/murasaki.svg?branch=master)](https://travis-ci.org/midori-rb/murasaki) |
| [![Test Coverage](https://api.codeclimate.com/v1/badges/f976d625994fa33523b3/test_coverage)](https://codeclimate.com/github/midori-rb/midori.rb) | [![Test Coverage](https://api.codeclimate.com/v1/badges/cfb6d9b359dcb7457eec/test_coverage)](https://codeclimate.com/github/midori-rb/midori-contrib) | [![Test Coverage](https://api.codeclimate.com/v1/badges/d0dc1bc4a3e38bd4f2b9/test_coverage)](https://codeclimate.com/github/midori-rb/murasaki) | [![Test Coverage](https://api.codeclimate.com/v1/badges/0035138294cf3a6fdd07/test_coverage)](https://codeclimate.com/github/midori-rb/http_parser.rb/test_coverage) |
| [![Maintainability](https://api.codeclimate.com/v1/badges/f976d625994fa33523b3/maintainability)](https://codeclimate.com/github/midori-rb/midori.rb) | [![Maintainability](https://api.codeclimate.com/v1/badges/cfb6d9b359dcb7457eec/maintainability)](https://codeclimate.com/github/midori-rb/midori-contrib) | [![Maintainability](https://api.codeclimate.com/v1/badges/d0dc1bc4a3e38bd4f2b9/maintainability)](https://codeclimate.com/github/midori-rb/murasaki) | [![Maintainability](https://api.codeclimate.com/v1/badges/0035138294cf3a6fdd07/maintainability)](https://codeclimate.com/github/midori-rb/http_parser.rb/maintainability) |
| [![Dependency Status](https://gemnasium.com/badges/github.com/midori-rb/midori.rb.svg)](https://gemnasium.com/github.com/midori-rb/midori.rb) | [![Dependency Status](https://gemnasium.com/badges/github.com/midori-rb/midori-contrib.svg)](https://gemnasium.com/github.com/midori-rb/midori-contrib) | [![Dependency Status](https://gemnasium.com/badges/github.com/midori-rb/murasaki.svg)](https://gemnasium.com/github.com/midori-rb/murasaki) | [![Dependency Status](https://gemnasium.com/badges/github.com/midori-rb/http_parser.rb.svg)](https://gemnasium.com/github.com/midori-rb/http_parser.rb) |
| [![doc](http://inch-ci.org/github/midori-rb/midori.rb.svg?branch=master)](http://inch-ci.org/github/midori-rb/midori.rb) | [![doc](http://inch-ci.org/github/midori-rb/midori-contrib.svg?branch=master)](http://inch-ci.org/github/midori-rb/midori-contrib) | [![doc](http://inch-ci.org/github/midori-rb/murasaki.svg?branch=master)](http://inch-ci.org/github/midori-rb/murasaki) | [![doc](http://inch-ci.org/github/midori-rb/http_parser.svg?branch=master)](http://inch-ci.org/github/midori-rb/http_parser.rb) |
| [![Gem Version](https://img.shields.io/gem/v/midori.rb.svg?maxAge=43200)](https://rubygems.org/gems/midori.rb) | [![Gem Version](https://img.shields.io/gem/v/midori-contrib.svg?maxAge=43200)](https://rubygems.org/gems/midori-contrib) | [![Gem Version](https://img.shields.io/gem/v/murasaki.svg?maxAge=43200)](https://rubygems.org/gems/murasaki) | [![Gem Version](https://img.shields.io/gem/v/midori_http_parser.svg?maxAge=43200)](https://rubygems.org/gems/midori_http_parser) |
| [![license](https://img.shields.io/github/license/midori-rb/midori.rb.svg?maxAge=2592000)]() | [![license](https://img.shields.io/github/license/midori-rb/midori-contrib.svg?maxAge=2592000)]() | [![license](https://img.shields.io/github/license/midori-rb/murasaki.svg?maxAge=2592000)]() | [![license](https://img.shields.io/github/license/midori-rb/http_parser.rb.svg?maxAge=2592000)]() |

## Requirements

- **Ruby** >= 2.2.6

## Installation

```bash
gem install midori.rb
```

**With Bundler**

```ruby
gem 'midori.rb'
```

```bash
bundle install
```

## FAQ

### Performance

Following benchmark results testing `{msg: "Hello"}` JSON response by visiting `GET /` with a **single-core, 4GB memory, UCloud Linux instance**.

**Note: Performance under Mac OS X needs to be further improved. `wrk` gives very bad performance result, but `ab` gives a good one. The following result is tested under Linux.**

| framework                    | version | req/s   |
| :--------------------------- | :------ | :------ |
| Rails (Thin, Ruby)           | 5.0.0.1 | 521.58  |
| Rails (API Mode, Thin, Ruby) | 5.0.0.1 | 760.03  |
| Sinatra (Thin, Ruby)         | 2.0.0   | 1912.23 |
| express.js (Node.js)         | 4.15.3  | 4944.58 |
| midori (Ruby)                | 0.2.4   | 3937.08 |

### Name

The name **midori** comes from **midori machi**, which was the place I stay on my first travel to Tokyo.

### Semantic Versioning

Version consists of four numbers:

|                 |     Milestone     |          Major           |    Minor    |  Patch   |
| --------------- | :---------------: | :----------------------: | :---------: | :------: |
| **Example**     |        1.         |            2.            |     1.      |    5     |
| **Explanation** | Milestone version | Incompatible API changes | Add feature | Fix bugs |

**Note: Before version v1.0, there's no minor version API compatible ensuring.**

### Contributing

See [Contributing Guidelines](CONTRIBUTING.md) before you leave any comment.

### Tutorial & Example

There is an unfinished tutorial available [here](https://github.com/midori-rb/midori.rb/tree/master/tutorial).

There is also an example showing how to use midori with a todo-list web app available [here](https://github.com/midori-rb/midori-todo-example).

## Roadmap

**Development roadmap has been moved [here](https://github.com/midori-rb/midori.rb/wiki/Roadmap).**


**Detailed release notes for published versions can be seen [here](https://github.com/midori-rb/midori.rb/releases).**

## Midori 2 Goals

1. Support HTTP/2
2. Add MVC abstraction example with scaffold
3. Improve performance of eventloop
4. More examples on using midori

