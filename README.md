# Rails On Couchbase

A Rails Project providing a base rails setup integrated and optimized for CouchBase.


## Requirements (at the time of writing.)

1. ruby - 1.9.3p194
2. rubygem - 1.8.23
3. libcouchbase - 1.1.0dp


Note: As we will be using couchbase-model 0.1.0, it has a dependency for couchbase ~> 1.2.0.dp.  That version of couchbase requires the libcouchbase 1.1.0dp version.  After getting educated by @avsej I was able to build libcouchbase 1.1.0dp using the following command: 

<pre><code>brew install https://raw.github.com/couchbase/homebrew/preview/Library/Formula/libcouchbase.rb"</code></pre>

A few other things to note that are not clearly posted on Couchbase when creating a new app from scratch:

**Configure your application**
The important thing here is to avoid loading ActiveRecord. One way to do this is with the --skip-active-record switch. So you'd create your app skeleton like so:

<pre><code>rails new my_app --skip-active-record</code></pre>

Alternatively, if you've already created your app (or just want to know what this actually does), have a look at config/application.rb and change the first lines from this:

<pre><code>require "rails/all"</code></pre>
to this:

<pre><code>require "action_controller/railtie"
require "action_mailer/railtie"
require "active_resource/railtie"
require "rails/test_unit/railtie"</code></pre>


## Usage

More coming soon.  The primary goal of this project is to provide a good well-documented solid foundational rails application configured to use Couchbase.  As I am very new to rails programming, I welcome all the help I can get.  Remember this is for newbies to learn from and use as a platform to start their rails development.

## Change Log
05/01/2012 - Updated README.md, Edited configuration for application and cleaned up directories.

## Open Source License
Copyright (C) 2012 DigitalRoyale. William Fleming

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.