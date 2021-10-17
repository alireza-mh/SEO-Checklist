### Prerender
Prerender is a technology that helps web applications which has been implemented with javascript only and SPA technology to got rendered as a html files for search engines.
Prerender simply try to render pages when the request from the search engines initiated and try to serve the rendered html files to the crawler. Also it's good practice to cache the pages before hand so it serve as fast as possible.

#### Debug
You just need to send a GET request with user-agent of google bot and see what is getting returned. In case you see the rendered HTML everything is working fine.
Also be aware to not render any js/css files since there is no need for them also if they get rendered in Prerenderer it would be cause a problem (wrap every code inside of `pre` tag) in mobile friendly test of the google.