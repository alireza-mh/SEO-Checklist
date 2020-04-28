## SEO Checklist

this repo is intended to help with some SEO suggestion and help you as a checklist for starting SEO on your site and web applications.

- [ ] Appropriate Domin Dah...! 
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

- [ ] `sitemap.xml` file can help crawlers to find webpages and also understand the priority you have in mind. if the name is not common here you can add `Sitemap` property inside `robots.txt` [more info](https://stackoverflow.com/questions/23041115/what-should-be-the-name-of-sitemap-file-while-submitting-to-google-webmasters)
```txt
# Group 2
User-agent: *
Allow: /

Sitemap: http://www.example.com/sitemap.xml
```


- [ ] Find good keywords. it's gonna take a while to find good keywords that help you rank well on search engines try to use keywords and check your hypothesize with tools such as alexa and google trend. Find keywords that is relevant to your site and business and don't try to spend too much time on keywords that your competitors work on them for quite some times, start with easy win keywords at first.

- [ ] Keep your site update. try to regulary update your site content and don't copy and paste content from others, If you do google will detect your content as a duplicate and you gonna get minus point and get punished. keep them original as possible or try to write your understanding from a article you read. try to include intended keyword inside your article
