<div align="center">

  # gunhoon.log

  Gunhoon Dev Blog

</div>


## Quick Start

To set up your environment to develop the Jekyll site:

1. Use Docker for Ruby:

    ```bash
    docker run --rm -it -v "$PWD":/opt/jekyll -w /opt/jekyll -p 4000:4000 ruby:3.3 bash
    ```

2. Install the required gems in a Gemfile:

    ```bash
    bundle install
    ```

3. Build your Jekyll site locally:

    ```bash
    bundle exec jekyll serve --host 0.0.0.0
    ```

4. Browse to http://0.0.0.0:4000.
