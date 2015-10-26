# Crosspost to Medium Generator for Jekyll and Octopress

This plugin makes it possible to automatically syndicate your posts to [Medium](https://medium.com) from your Jekyll and Octopress projects.

## Setup

1. Set up a Medium account (if you don’t already have one)
2. Go to [your settings page](https://medium.com/me/settings) and look for "Integration Tokens". Generate one. Save it to your Environment Variables as MEDIUM_INTEGRATION_TOKEN
3. Visit `https://api.medium.com/v1/me?accessToken=`, addint your Integration Token to the end of that URL
4. Grab the id from the JSON provided and save that to your Environment Variables as MEDIUM_USER_ID
5. Copy `crosspost_to_medium.rb` to your `plugins` folder

## Crossposting

Add `crosspost_to_medium: true` to the front matter for any post you would like to crosspost to Medium.

Crossposted files will be logged in `.cache/medium_crossposted.yml`, so make sure that file gets checked into your Git repo if you work from multiple computers. That will enssure you never crosspost an entry more than once.

## Credits

Many thanks to Jeremy Keith for [sharing his process](https://adactio.com/journal/9694) (and [PHP code](https://gist.github.com/adactio/c174a4a68498e30babfd)) for getting this working on his own site.