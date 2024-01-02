# NSU SysPro GitHub pages

- Website: https://nsu-syspro.github.io
- Theme: [nsu-syspro/minima](https://github.com/nsu-syspro/minima)
- Powered by [Jekyll](https://jekyllrb.com)

## Local development

### Prerequisites

> [!NOTE]
> For more information see
> [Testing your GitHub Pages site locally with Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll)

- Install [Jekyll](https://jekyllrb.com/docs/installation/)
- Clone this repo
- Run `./bootstrap` script

### Starting server locally

To start server locally run `./start` script:

```console
$ ./start 
Fetching https://github.com/nsu-syspro/minima.git
Fetching gem metadata from https://rubygems.org/..........
Resolving dependencies...
Bundle updated!
Configuration file: _config.yml
To use retry middleware with Faraday v2.0+, install `faraday-retry` gem
            Source: /path/to/nsu-syspro.github.io
       Destination: /path/to/nsu-syspro.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
      Remote Theme: Using theme nsu-syspro/minima
       Jekyll Feed: Generating feed for posts
                    done in 1.376 seconds.
 Auto-regeneration: enabled for '/path/to/nsu-syspro.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

Development server will start at http://127.0.0.1:4000.

### Using local theme repo

By default Jekyll will fetch theme from [nsu-syspro/minima](https://github.com/nsu-syspro/minima) GitHub repo.

To override this behavior and use local copy of that repo instead
pass path to local repo as an argument to `./start` script:

```console
$ ./start ../minima
Fetching gem metadata from https://rubygems.org/..........
Resolving dependencies...
Bundle updated!
Configuration file: _config.yml
Configuration file: _config_local.yml
To use retry middleware with Faraday v2.0+, install `faraday-retry` gem
            Source: /path/to/nsu-syspro.github.io
       Destination: /path/to/nsu-syspro.github.io/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
      Remote Theme: "none" is not a valid remote theme
       Jekyll Feed: Generating feed for posts
                    done in 0.168 seconds.
 Auto-regeneration: enabled for '/path/to/nsu-syspro.github.io'
    Server address: http://127.0.0.1:4000/
  Server running... press ctrl-c to stop.
```

> [!NOTE]
> Jekyll will complain about "remote theme" which is fine
> ```
> Remote Theme: "none" is not a valid remote theme
> ```
