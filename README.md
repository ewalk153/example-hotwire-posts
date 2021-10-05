# README

Simple playground of [turbo-rails](https://github.com/hotwired/turbo-rails), [hotwire-rails](https://github.com/hotwired/hotwire-rails) to learn about [Hotwire](https://hotwired.dev/).

Inline creation, and edit via turbo/hotwire.

Small use of stimulus to reset the form on the client.

Launch redis easily with: `bin/dev-docker-redis`

# Odd things, I think are correct

We use two different broadcast channels for post changes:
1. `broadcasts` to update on the post show page
2. "posts" to update the index page

# Key commands used to generate this project
```bash
bundle add hotwire-rails
bundle add turbo-rails
rails stimulus:install
rails turbo:install
```
And then adding `import "../controllers"` to `packs/application.js` to get stimulus running.

Also, the `<%= turbo_stream_from ... %>` and the `<%= turbo_frame_tag ... do %>` littered across the views.

# TODOs
- [ ] experiment with validation feedback
- [ ] deploy on heroku
- [ ] document the trace of a message starting in the broadcast concern all the way back through to the web client over websockets
- [ ] create a version that drops webpacker and uses [importmap-rails](https://github.com/rails/importmap-rails)
