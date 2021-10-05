# README

Simple playground of turbo-rails, hotwire-rails.

Inline creation, and edit via turbo/hotwire.

Small use of stimulus to reset the form on the client.

TODO: experiment with validation feedback.

Launch redis easily with: `docker run --rm -it -p 6379:6379 redis:latest`

# Odd things, I think are correct

We use two different broadcast channels for post changes:
1. `broadcasts` to update on the post show page
2. "posts" to update the index page ()

# Key commands used to generate this project
```bash
bundle add hotwire-rails
bundle add turbo-rails
rails stimulus:install
rails turbo:install
```
And then adding `import "../controllers"` to `packs/application.js` to get stimulus running.

Also, the `<%= turbo_stream_from ... %>` and the `<%= turbo_frame_tag ... do %>` littered across the views.
