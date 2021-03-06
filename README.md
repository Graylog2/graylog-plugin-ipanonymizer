IP Address Anonymizer Plugin for Graylog
========================================

[![Build Status](https://travis-ci.org/Graylog2/graylog-plugin-ipanonymizer.svg)](https://travis-ci.org/Graylog2/graylog-plugin-ipanonymizer)

A Graylog plugin that replaces the last octet of IP addresses in messages with `xxx`.

**Note:** This plugin will be replaced in the future with [processing pipelines](http://docs.graylog.org/en/2.0/pages/pipelines.html).
Please consider testing them and submit feedback.

**Required Graylog version:** 2.0 and later

Please use version 1.1.2 of this plugin if you are still running Graylog 1.x

## Installation

[Download the plugin](https://github.com/Graylog2/graylog-plugin-ipanonymizer/releases)
and place the `.jar` file in your Graylog plugin directory. The plugin directory
is the `plugins/` folder relative from your `graylog-server` directory by default
and can be configured in your `graylog.conf` file.

Restart `graylog-server` and you are done.

## Build

This project is using Maven and requires Java 8 or higher.

You can build a plugin (JAR) with `mvn package`.

DEB and RPM packages can be build with `mvn jdeb:jdeb` and `mvn rpm:rpm` respectively.

## Plugin Release

We are using the maven release plugin:

```
$ mvn release:prepare
[...]
$ mvn release:perform
```

This sets the version numbers, creates a tag and pushes to GitHub. TravisCI will build the release artifacts and upload to GitHub automatically.
