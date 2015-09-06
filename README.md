# go-url-fuzzer

Status: **Work in progress**, not ready yet

Discover hidden files and directories on a web server. The application tries to find url relative paths of the given website by comparing them with a given set. Go-url-fuzzer is inspired by [Indir Scanner](http://indir.uw-team.org/), which is written in Perl. Comparing to Indir Scanner, the application supports concurrent url fuzzing.

## Features

* Fuzz url set from an input file
* Concurrent relative path search
* Configurable number of fuzzing workers
* Configurable time wait periods between fuzz tests per worker
* Custom HTTP headers support
* Different HTTP method support
* HTML url fuzzing reports

## Usage

~~~
Usage: go-url-fuzzer [options] -f <fuzz-set-file> <base-url>

fuzz-set-file  File containing fuzz entry set, one entry per line
base-url  Base url of the examined web

Options:
  -w Time wait period between fuzz tests per worker, in seconds
  -m Comma-separated HTTP methods used in tests (GET, POST, PUT, DELETE, HEAD, OPTIONS)
  -h "Header: value", custom HTTP header added to every fuzz request
  -t Fuzzed url response timeout, in seconds

Example:

~~~

## License

The MIT License (MIT)

Copyright (c) 2015 Marcin Tojek

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
