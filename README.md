[![build status](https://secure.travis-ci.org/cucumber/cucumber-html.svg)](http://travis-ci.org/cucumber/cucumber-html)

Cucumber-HTML is a cross-platform HTML formatter for all the Cucumber implementations. It is
currently only used by Cucumber-JVM ~and Cucumber.js, but may be used by other implementations later~.


> **Update Juli 2018**: `cucumber-html` has been inlined into `cucumber-jvm`. 
> **Update August 2017**: Cucumber.js does not use this project.
>
> The current thinking is to replace formatters like the HTML formatter and Pretty formatter with event-based, all-platform compatible utilities in the spirit of [cucumber-pretty-formatter](https://github.com/cucumber/cucumber-pretty-formatter) (a work-in-progress).

## Prerequisites

The formatter generates HTML that conforms to the HTML5 specification, so you need a modern browser to see the results.

## Generating PDF

This formatter replaces Cucumber's old PDF formatter. You can easily turn a HTML report into a PDF with the excellent [wkhtmltopdf](https://wkhtmltopdf.org/):

    wkhtmltopdf cucumber-report.html cucumber-report.pdf

## Release process

* Make sure `pom.xml` has a `X.Y.Z-SNAPSHOT` version
* Make sure `package.json` has a `X.Y.Z` version

Now release:

    make release
