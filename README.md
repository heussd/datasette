# Datasette

[![PyPI](https://img.shields.io/pypi/v/datasette.svg)](https://pypi.org/project/datasette/)
[![Travis CI](https://travis-ci.org/simonw/datasette.svg?branch=master)](https://travis-ci.org/simonw/datasette)
[![Documentation Status](https://readthedocs.org/projects/datasette/badge/?version=latest)](http://datasette.readthedocs.io/en/latest/?badge=latest)
[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://github.com/simonw/datasette/blob/master/LICENSE)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://black.readthedocs.io/en/stable/)

*A tool for exploring and publishing data*

Datasette is a tool for exploring and publishing data. It helps people take data of any shape or size and publish that as an interactive, explorable website and accompanying API.

Datasette is aimed at data journalists, museum curators, archivists, local governments and anyone else who has data that they wish to share with the world.

[Explore a demo](https://fivethirtyeight.datasettes.com/fivethirtyeight), watch [a video about the project](https://www.youtube.com/watch?v=pTr1uLQTJNE) or try it out by [uploading and publishing your own CSV data](https://simonwillison.net/2019/Apr/23/datasette-glitch/).

* Comprehensive documentation: http://datasette.readthedocs.io/
* Examples: https://github.com/simonw/datasette/wiki/Datasettes
* Live demo of current master: https://latest.datasette.io/

## News

 * 13th July 2019: [Single sign-on against GitHub using ASGI middleware](https://simonwillison.net/2019/Jul/14/sso-asgi/) talks about the implementation of [datasette-auth-github](https://github.com/simonw/datasette-auth-github) in more detail.
 * 7th July 2019: [Datasette 0.29](https://datasette.readthedocs.io/en/stable/changelog.html#v0-29) - ASGI, new plugin hooks, facet by date and much, much more...
   * [datasette-auth-github](https://github.com/simonw/datasette-auth-github) - a new plugin for Datasette 0.29 that lets you require users to authenticate against GitHub before accessing your Datasette instance. You can whitelist specific users, or you can restrict access to members of specific GitHub organizations or teams.
   * [datasette-cors](https://github.com/simonw/datasette-cors) - a plugin that lets you configure CORS access from a list of domains (or a set of domain wildcards) so you can make JavaScript calls to a Datasette instance from a specific set of other hosts.
 * 23rd June 2019: [Porting Datasette to ASGI, and Turtles all the way down](https://simonwillison.net/2019/Jun/23/datasette-asgi/)
 * 21st May 2019: The anonymized raw data from [the Stack Overflow Developer Survey 2019](https://stackoverflow.blog/2019/05/21/public-data-release-of-stack-overflows-2019-developer-survey/) has been [published in partnership with Glitch](https://glitch.com/culture/discover-insights-explore-developer-survey-results-2019/), powered by Datasette.
 * 19th May 2019: [Datasette 0.28](https://datasette.readthedocs.io/en/stable/changelog.html#v0-28) - a salmagundi of new features!
   * No longer immutable! Datasette now supports [databases that change](https://datasette.readthedocs.io/en/stable/changelog.html#supporting-databases-that-change).
   * [Faceting improvements](https://datasette.readthedocs.io/en/stable/changelog.html#faceting-improvements-and-faceting-plugins) including facet-by-JSON-array and the ability to define custom faceting using plugins.
   * [datasette publish cloudrun](https://datasette.readthedocs.io/en/stable/changelog.html#datasette-publish-cloudrun) lets you publish databases to Google's new Cloud Run hosting service.
   * New [register_output_renderer](https://datasette.readthedocs.io/en/stable/changelog.html#register-output-renderer-plugins) plugin hook for adding custom output extensions to Datasette in addition to the default `.json` and `.csv`.
   * Dozens of other smaller features and tweaks - see [the release notes](https://datasette.readthedocs.io/en/stable/changelog.html#v0-28) for full details.
   * Read more about this release here: [Datasette 0.28—and why master should always be releasable](https://simonwillison.net/2019/May/19/datasette-0-28/)
 * 24th February 2019: [
sqlite-utils: a Python library and CLI tool for building SQLite databases](https://simonwillison.net/2019/Feb/25/sqlite-utils/) - a partner tool for easily creating SQLite databases for use with Datasette.
 * 31st Janary 2019: [Datasette 0.27](https://datasette.readthedocs.io/en/latest/changelog.html#v0-27) - `datasette plugins` command, newline-delimited JSON export option, new documentation on [The Datasette Ecosystem](https://datasette.readthedocs.io/en/latest/ecosystem.html).
 * 10th January 2019: [Datasette 0.26.1](http://datasette.readthedocs.io/en/latest/changelog.html#v0-26-1) - SQLite upgrade in Docker image, `/-/versions` now shows SQLite compile options.
 * 2nd January 2019: [Datasette 0.26](http://datasette.readthedocs.io/en/latest/changelog.html#v0-26) - minor bug fixes, `datasette publish now --alias` argument.
* 18th December 2018: [Fast Autocomplete Search for Your Website](https://24ways.org/2018/fast-autocomplete-search-for-your-website/) - a new tutorial on using Datasette to build a JavaScript autocomplete search engine.
* 3rd October 2018: [The interesting ideas in Datasette](https://simonwillison.net/2018/Oct/4/datasette-ideas/) - a write-up of some of the less obvious interesting ideas embedded in the Datasette project.
* 19th September 2018: [Datasette 0.25](http://datasette.readthedocs.io/en/latest/changelog.html#v0-25) - New plugin hooks, improved database view support and an easier way to use more recent versions of SQLite.
* 23rd July 2018: [Datasette 0.24](http://datasette.readthedocs.io/en/latest/changelog.html#v0-24) - a number of small new features
* 29th June 2018: [datasette-vega](https://github.com/simonw/datasette-vega), a new plugin for visualizing data as bar, line or scatter charts
* 21st June 2018: [Datasette 0.23.1](http://datasette.readthedocs.io/en/latest/changelog.html#v0-23-1) - minor bug fixes
* 18th June 2018: [Datasette 0.23: CSV, SpatiaLite and more](http://datasette.readthedocs.io/en/latest/changelog.html#v0-23) - CSV export, foreign key expansion in JSON and CSV, new config options, improved support for SpatiaLite and a bunch of other improvements
* 23rd May 2018: [Datasette 0.22.1 bugfix](https://github.com/simonw/datasette/releases/tag/0.22.1) plus we now use [versioneer](https://github.com/warner/python-versioneer)
* 20th May 2018: [Datasette 0.22: Datasette Facets](https://simonwillison.net/2018/May/20/datasette-facets)
* 5th May 2018: [Datasette 0.21: New _shape=, new _size=, search within columns](https://github.com/simonw/datasette/releases/tag/0.21)
* 25th April 2018: [Exploring the UK Register of Members Interests with SQL and Datasette](https://simonwillison.net/2018/Apr/25/register-members-interests/) - a tutorial describing how [register-of-members-interests.datasettes.com](https://register-of-members-interests.datasettes.com/) was built ([source code here](https://github.com/simonw/register-of-members-interests))
* 20th April 2018: [Datasette plugins, and building a clustered map visualization](https://simonwillison.net/2018/Apr/20/datasette-plugins/) - introducing Datasette's new plugin system and [datasette-cluster-map](https://pypi.org/project/datasette-cluster-map/), a plugin for visualizing data on a map
* 20th April 2018: [Datasette 0.20: static assets and templates for plugins](https://github.com/simonw/datasette/releases/tag/0.20)
* 16th April 2018: [Datasette 0.19: plugins preview](https://github.com/simonw/datasette/releases/tag/0.19)
* 14th April 2018: [Datasette 0.18: units](https://github.com/simonw/datasette/releases/tag/0.18)
* 9th April 2018: [Datasette 0.15: sort by column](https://github.com/simonw/datasette/releases/tag/0.15)
* 28th March 2018: [Baltimore Sun Public Salary Records](https://simonwillison.net/2018/Mar/28/datasette-in-the-wild/) - a data journalism project from the Baltimore Sun powered by Datasette - source code [is available here](https://github.com/baltimore-sun-data/salaries-datasette)
* 27th March 2018: [Cloud-first: Rapid webapp deployment using containers](https://wwwf.imperial.ac.uk/blog/research-software-engineering/2018/03/27/cloud-first-rapid-webapp-deployment-using-containers/) - a tutorial covering deploying Datasette using Microsoft Azure by the Research Software Engineering team at Imperial College London
* 28th January 2018: [Analyzing my Twitter followers with Datasette](https://simonwillison.net/2018/Jan/28/analyzing-my-twitter-followers/) - a tutorial on using Datasette to analyze follower data pulled from the Twitter API
* 17th January 2018: [Datasette Publish: a web app for publishing CSV files as an online database](https://simonwillison.net/2018/Jan/17/datasette-publish/)
* 12th December 2017: [Building a location to time zone API with SpatiaLite, OpenStreetMap and Datasette](https://simonwillison.net/2017/Dec/12/building-a-location-time-zone-api/)
* 9th December 2017: [Datasette 0.14: customization edition](https://github.com/simonw/datasette/releases/tag/0.14)
* 25th November 2017: [New in Datasette: filters, foreign keys and search](https://simonwillison.net/2017/Nov/25/new-in-datasette/)
* 13th November 2017: [Datasette: instantly create and publish an API for your SQLite databases](https://simonwillison.net/2017/Nov/13/datasette/)

## Installation

    pip3 install datasette

Datasette requires Python 3.5 or higher. We also have [detailed installation instructions](https://datasette.readthedocs.io/en/stable/installation.html) covering other options such as Docker.

## Basic usage

    datasette serve path/to/database.db

This will start a web server on port 8001 - visit http://localhost:8001/ to access the web interface.

`serve` is the default subcommand, you can omit it if you like.

Use Chrome on OS X? You can run datasette against your browser history like so:

     datasette ~/Library/Application\ Support/Google/Chrome/Default/History

Now visiting http://localhost:8001/History/downloads will show you a web interface to browse your downloads data:

![Downloads table rendered by datasette](https://static.simonwillison.net/static/2017/datasette-downloads.png)

## datasette serve options

    $ datasette serve --help

    Usage: datasette serve [OPTIONS] [FILES]...

      Serve up specified SQLite database files with a web UI

    Options:
      -i, --immutable PATH      Database files to open in immutable mode
      -h, --host TEXT           host for server, defaults to 127.0.0.1
      -p, --port INTEGER        port for server, defaults to 8001
      --debug                   Enable debug mode - useful for development
      --reload                  Automatically reload if database or code change detected -
                                useful for development
      --cors                    Enable CORS by serving Access-Control-Allow-Origin: *
      --load-extension PATH     Path to a SQLite extension to load
      --inspect-file TEXT       Path to JSON file created using "datasette inspect"
      -m, --metadata FILENAME   Path to JSON file containing license/source metadata
      --template-dir DIRECTORY  Path to directory containing custom templates
      --plugins-dir DIRECTORY   Path to directory containing custom plugins
      --static STATIC MOUNT     mountpoint:path-to-directory for serving static files
      --memory                  Make :memory: database available
      --config CONFIG           Set config option using configname:value
                                datasette.readthedocs.io/en/latest/config.html
      --version-note TEXT       Additional note to show on /-/versions
      --help-config             Show available config options
      --help                    Show this message and exit.

## metadata.json

If you want to include licensing and source information in the generated datasette website you can do so using a JSON file that looks something like this:

    {
        "title": "Five Thirty Eight",
        "license": "CC Attribution 4.0 License",
        "license_url": "http://creativecommons.org/licenses/by/4.0/",
        "source": "fivethirtyeight/data on GitHub",
        "source_url": "https://github.com/fivethirtyeight/data"
    }

Save this in `metadata.json` and run Datasette like so:

    datasette serve fivethirtyeight.db -m metadata.json

The license and source information will be displayed on the index page and in the footer. They will also be included in the JSON produced by the API.

## datasette publish

If you have [Heroku](https://heroku.com/), [Google Cloud Run](https://cloud.google.com/run/) or [Zeit Now v1](https://zeit.co/now) configured, Datasette can deploy one or more SQLite databases to the internet with a single command:

    datasette publish heroku database.db

Or:

    datasette publish cloudrun database.db

This will create a docker image containing both the datasette application and the specified SQLite database files. It will then deploy that image to Heroku or Cloud Run and give you a URL to access the resulting website and API.

See [Publishing data](https://datasette.readthedocs.io/en/stable/publish.html) in the documentation for more details.
