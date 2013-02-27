# Eden Code Standards Guide

http://baby-com-br.github.com/code-standards

This project uses the Github Pages to generate the site with the Eden Code
Standards Guide.

## Running locally

1. Execute `bundle install`
2. Execute `rake site:run`
3. Visit `localhost:4000`

The `site:run` Rake task will run the Jekyll server with the `--auto --pygments`
options, and will run the `sass --watch` with the correct source and destination.
