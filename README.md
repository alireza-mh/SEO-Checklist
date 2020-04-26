## SEO Checklist

this repo is intended to help with some SEO suggestion and help you as a checklist for starting SEO on your site and web applications.

- [] Appropriate Domin Dah...! 
good domain name can boost your SEO rank and make it easy or hard for user to revisit your site.
- [ ] Appropriate title for Pages (some convention in embed company name among title exam: Home | Company)‍‍‍‍‍‍

```html
<head>
  <title>Home | company</title>
</head>
```

- [ ] include meta description and meta tags.

```html
<head>
  <meta
    name="description"
    content="This is an example of a meta description. This will often show up in search results."
  />
</head>
```
- [ ] `robot.txt` file. it will be used bye search engines and you can have black list for path that you don't want to index via search engines. some  [more info](https://moz.com/learn/seo/robotstxt)

#### basic format
```txt
User-agent: [user-agent name]Disallow: [URL string not to be crawled]
```
```txt
User-agent: *
Disallow:
```

