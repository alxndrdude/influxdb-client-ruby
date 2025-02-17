## 3.1.0 [unreleased]

## 3.0.0 [2023-12-05]

### Bug Fixes
1. [#131](https://github.com/influxdata/influxdb-client-ruby/pull/131): Convert time objects present in fields to integer. Prior to this change the timestamps were converted to strings

## 2.9.0 [2022-12-01]

:warning: The client can be used as a resource:

    InfluxDB2::Client.use('https://localhost:8086', 'my-token') do |client|
        client.do_something
    end

### Features
1. [#126](https://github.com/influxdata/influxdb-client-ruby/pull/126): Add `Task` API
1. [#127](https://github.com/influxdata/influxdb-client-ruby/pull/127): Client can be used as a resource

### Bug Fixes
1. [#123](https://github.com/influxdata/influxdb-client-ruby/pull/123): Duplicate columns warning shows in improper situations
1. [#124](https://github.com/influxdata/influxdb-client-ruby/pull/124): Query return type is `Array` instead of `Hash`

## 2.8.0 [2022-10-27]

### Features
1. [#118](https://github.com/influxdata/influxdb-client-ruby/pull/118): Add `FluxRecord.row` which stores response data in a array

## 2.7.0 [2022-07-29]

### Features
1. [#106](https://github.com/influxdata/influxdb-client-ruby/pull/106): Add logging for HTTP requests

### Others
1. [#108](https://github.com/influxdata/influxdb-client-ruby/pull/108): Use local repository for `influxdb-client-apis` development

### CI
1. [#109](https://github.com/influxdata/influxdb-client-ruby/pull/109): Add Ruby 3.1 into CI

## 2.6.0 [2022-06-24]

### Bug Fixes
1. [#105](https://github.com/influxdata/influxdb-client-ruby/pull/105): Add missing require for `PatchBucketRequest` model

## 2.5.0 [2022-05-20]

### Breaking Changes
1. [#103](https://github.com/influxdata/influxdb-client-ruby/pull/103): Rename `InvocableScripts` to `InvokableScripts`

## 2.4.0 [2022-04-19]

### Features
1. [#101](https://github.com/influxdata/influxdb-client-ruby/pull/101): Add `InvokableScriptsApi` to create, update, list, delete and invoke scripts by seamless way

## 2.3.0 [2022-03-18]

### Bug Fixes
1. [#99](https://github.com/influxdata/influxdb-client-ruby/pull/99): Add missing `PatchBucketRequest` model

### CI
1. [#100](https://github.com/influxdata/influxdb-client-ruby/pull/100): Use new Codecov uploader for reporting code coverage

## 2.2.0 [2022-02-18]

### Features
1. [#96](https://github.com/influxdata/influxdb-client-ruby/pull/96): Add support for Parameterized Queries

### Bug Fixes
1. [#97](https://github.com/influxdata/influxdb-client-ruby/pull/97): Add missing PermissionResources from Cloud API definition

### Documentation
1. [#96](https://github.com/influxdata/influxdb-client-ruby/pull/96): Add Parameterized Queries example

## 2.1.0 [2021-10-22]

### Features
1. [#93](https://github.com/influxdata/influxdb-client-ruby/pull/93): Add `PingApi` to check status of OSS and Cloud instance

### CI
1. [#91](https://github.com/influxdata/influxdb-client-ruby/pull/91): Switch to next-gen CircleCI's convenience images
1. [#95](https://github.com/influxdata/influxdb-client-ruby/pull/95): Update `jruby` to `9.3.1.0-jdk11`

## 2.0.0 [2021-09-13]

### Bug Fixes
1. [#90](https://github.com/influxdata/influxdb-client-ruby/pull/90): Fix parse text plain 503 error response  
1. [#89](https://github.com/influxdata/influxdb-client-ruby/pull/89): Correct redirect location

### Breaking Changes
Due to a security reason `Authorization` header is not forwarded when redirect leads to a different domain.
To overcome this limitation you have to set the client property `redirect_forward_authorization` to `true`.

### Features
1. [#89](https://github.com/influxdata/influxdb-client-ruby/pull/89): `Authorization` header is not forwarded when redirect leads to a different domain
 
## 1.17.0 [2021-08-20]

### Bug Fixes
1. [#87](https://github.com/influxdata/influxdb-client-ruby/pull/87): Parsing infinite numbers

## 1.16.0 [2021-07-09]

### Bug Fixes
1. [#86](https://github.com/influxdata/influxdb-client-ruby/pull/86): Uninitialized `set` for models

## 1.15.0 [2021-06-04]

### API
1. [#79](https://github.com/influxdata/influxdb-client-ruby/pull/79): Update swagger generator to 5.1.1
1. [#82](https://github.com/influxdata/influxdb-client-ruby/pull/82): Use [openapi](https://github.com/influxdata/openapi) repository as a source for InfluxDB API definition

## 1.14.0 [2021-04-30]

### API
1. [#77](https://github.com/influxdata/influxdb-client-ruby/pull/77): Update swagger to latest version

### CI
1. [#78](https://github.com/influxdata/influxdb-client-ruby/pull/78): Add build configuration for jruby

## 1.13.0 [2021-04-01]

### API
1. [#76](https://github.com/influxdata/influxdb-client-ruby/pull/76): Update swagger to latest version

## 1.12.1 [2021-03-05]

### Bug Fixes
1. [#74](https://github.com/influxdata/influxdb-client-ruby/pull/74): Avoid uses sources from parent path

## 1.12.0 [2021-03-05]

### Features
1. [#69](https://github.com/influxdata/influxdb-client-ruby/pull/69): Created `influxdb-client-apis` package for Management API
1. [#71](https://github.com/influxdata/influxdb-client-ruby/pull/71): Added possibility to specify the certification verification behaviour

### CI
1. [#73](https://github.com/influxdata/influxdb-client-ruby/pull/73): Updated stable image to `influxdb:latest` and nightly to `quay.io/influxdb/influxdb:nightly`

## 1.11.0 [2021-01-29]

### CI
1. [#63](https://github.com/influxdata/influxdb-client-ruby/pull/63): Updated default docker image to v2.0.3
1. [#65](https://github.com/influxdata/influxdb-client-ruby/pull/65): Added Ruby 3.0 into CI

## 1.10.0 [2020-12-04]

### Features
1. [#59](https://github.com/influxdata/influxdb-client-ruby/pull/59): CSV parser is able to parse export from UI

### CI
1. [#62](https://github.com/influxdata/influxdb-client-ruby/pull/62): Updated default docker image to v2.0.2

### Bug Fixes
1. [#61](https://github.com/influxdata/influxdb-client-ruby/pull/61): Query results has precision with nanosecond, e.g. '1970-01-01T00:00:00.000123456+00:00'

## 1.9.0 [2020-10-30]

### Features
1. [#55](https://github.com/influxdata/influxdb-client-runy/pull/55): Improved logging message for retries

## 1.8.0 [2020-10-02]

### Features
1. [#36](https://github.com/influxdata/influxdb-client-ruby/issues/36): Added support for default tags
1. [#53](https://github.com/influxdata/influxdb-client-ruby/pull/53): Default strategy for batching worker is best-effort

### API
1. [#50](https://github.com/influxdata/influxdb-client-ruby/pull/50): Default port changed from 9999 -> 8086
 
### Bug Fixes
1. [#52](https://github.com/influxdata/influxdb-client-ruby/pull/52): Fixed aborting of background threads

## 1.7.0 [2020-08-14]

### Features
1. [#47](https://github.com/influxdata/influxdb-client-ruby/pull/47): Added max_retries, max_retry_delay and exponential_base to WriteApi

## 1.6.0 [2020-07-17]

### Bug Fixes
1. [#42](https://github.com/influxdata/influxdb-client-ruby/pull/42): Fixed serialization of `\n`, `\r` and `\t` to Line Protocol, `=` is valid sign for measurement name  
1. [#44](https://github.com/influxdata/influxdb-client-ruby/pull/44): Fixed supporting of Ruby 2.2

## 1.5.0 [2020-06-19]

### API
1. [#41](https://github.com/influxdata/influxdb-client-ruby/pull/41): Updated swagger to latest version

## 1.4.0 [2020-05-15]

### Features

1. [#38](https://github.com/influxdata/influxdb-client-ruby/pull/38): Remove trailing slash from connection URL

### Documentation

1. [#37](https://github.com/influxdata/influxdb-client-ruby/pull/37): Fix documentation: replace references to InfluxDB module by InfluxDB2. Allow `require 'influxdb-client'`

## 1.3.0 [2020-04-17]

### Features

1. [#32](https://github.com/influxdata/influxdb-client-ruby/pull/32): Checks the health of a running InfluxDB instance by querying the /health

### Documentation

1. [#35](https://github.com/influxdata/influxdb-client-ruby/pull/35): Clarify how to use a client with InfluxDB 1.8

## 1.2.0 [2020-03-13]

### Features
1. [#23](https://github.com/influxdata/influxdb-client-ruby/issues/23): Added DeleteApi to delete time series data from InfluxDB.
1. [#24](https://github.com/influxdata/influxdb-client-ruby/issues/24): Added jitter_interval and retry_interval to WriteApi
1. [#26](https://github.com/influxdata/influxdb-client-ruby/issues/26): Set User-Agent to influxdb-client-ruby/VERSION for all requests

### Security
1. [#29](https://github.com/influxdata/influxdb-client-ruby/pull/29): Upgrade rake to version 12.3.3 - [CVE-2020-8130](https://github.com/advisories/GHSA-jppv-gw3r-w3q8)

### Bug Fixes
1. [#22](https://github.com/influxdata/influxdb-client-ruby/pull/22): Fixed batch write
1. [#28](https://github.com/influxdata/influxdb-client-ruby/pull/28): Correctly parse CSV where multiple results include multiple tables
1. [#30](https://github.com/influxdata/influxdb-client-ruby/pull/30): Send Content-Type headers

## 1.1.0 [2020-02-14]

### Features
1. [#14](https://github.com/influxdata/influxdb-client-ruby/issues/14): Added QueryApi
2. [#17](https://github.com/influxdata/influxdb-client-ruby/issues/17): Added possibility to stream query result
3. [#19](https://github.com/influxdata/influxdb-client-ruby/issues/19): Added WriteOptions and possibility to batch write
 
## 1.0.0.beta [2020-01-17]

### Features
1. [#4](https://github.com/influxdata/influxdb-client-ruby/pull/4): Added WriteApi that will be used for Fluentd plugin
 
