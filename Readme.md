# Docker Jekyll

## Installation
1. Install [Docker](https://docs.docker.com/engine/installation/)
2. Run the installer
  ```
  docker-compose run serve bundle exec jekyll new .
  ```
3. You have a Jekyll blog setup

## Deploying
1. Build the site
  ```
  docker-compose run build
  ```
2. The built site is in the _site directory

TODO: Also explain how to deploy on GitHub sites

## Helpful commands:
#### Draft new post

  ```
  docker-compose run draft "My New Page"
  ```

#### Publish a post

  ```
  # --date is optional
  docker-compose run publish _drafts/my-new-draft.md --date 2014-01-24
  ```

#### Unpublish a post

  ```
  docker-compose run unpublish _posts/2014-01-24-my-new-draft.md
  ```

#### Check SEO

  ```
  # -k are the keywords to check
  # -p is the post
  docker-compose run checkseo -k "welcome to jekyll" -p ../dist/welcome-to-jekyll.html
  ```
