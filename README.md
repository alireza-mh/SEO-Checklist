## SEO Checklist

this repo is intended to help with some SEO suggestions and help you as a checklist for starting SEO on your site and web applications.

- [ ] Appropriate Domain Dah...! 
A good domain name can boost your SEO rank and make it easy or hard for the user to revisit your site.
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

- [ ] `robot.txt` file. it will be used by search engines and you can have a blacklist for the path that you don't want to index via search engines. some  [more info](https://moz.com/learn/seo/robotstxt)
you can also validate your specific URLs with robots.txt on this  [address](https://www.google.com/webmasters/tools/robots-testing-tool). This is a tool provided by Google.


#### basic format
```txt
User-agent: [user-agent name]
Disallow: [URL string not to be crawled]
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


- [ ] Find good keywords. it's gonna take a while to find good keywords that help you rank well on search engines try to use keywords and check your hypothesize with tools such as Alexa and google trend. Find keywords that are relevant to your site and business and don't try to spend too much time on keywords that your competitors work on them for quite some time, start with easy win keywords at first.

- [ ] Keep your site update. try to regularly update your site content and don't copy and paste content from others, If you do google will detect your content as a duplicate and you gonna get a minus point and get punished. keep them original as possible or try to write your understanding from an article you read. try to include intended keyword inside your article

- [ ] Make your site fast. this can help with your ranking and conversion rate of your business. some fast ways and easy wins to make your site faster are listed below:

1 - use CDN to deliver your site according to user location

2 - optimization of image size and format. try to use image size that matches the design. for example, a card with 250x100 should not have an image with the original size of 1000x400. also in case of not using a transparent image try to use jpeg files. there are some sites that you can use for image optimization such as [tinypng](https://tinypng.com/) and [sqoosh](https://squoosh.app/) there are too many things to do but this seems enough for this part

3 - use cache header to make the second visit faster

4 - minify and remove unused js or CSS. here you can use webpack or postcss in case you are working with the latest techs of frontend or simply use [minifier](https://www.minifier.org/)

5 - use [AMP](https://developers.google.com/amp). with amp, your page gonna serve directly from google and really fast there are some pros and cons and we may cover it later on it own section

### Use open graph
This protocol has been proposed by Facebook. This protocol helps with sharing web site links in social media. this way any link that will share on twitter, Whatsapp and other platform gonna have title, description, or images.

#### The four required properties for every page are:

- `og:title` - The title of your object as it should appear within the graph, e.g., "The Rock".
- `og:type` - The type of your object, e.g., "video.movie". Depending on the type you specify, other properties may also be required.
- `og:image` - An image URL which should represent your object within the graph.
- `og:url` - The canonical URL of your object that will be used as its permanent ID in the graph, e.g., "http://www.imdb.com/title/tt0117500/".

### Tools
So after implementing all or some of the earlier suggestions you need to monitor your visit and gather data to see if they are effective or is there something else you need to do to achieve better results. 

#### Google analytics
This tool is must have on all websites and web apps. you can see user flow and also see all visits to your website. it provides all sorts of information such as unique user visits, bounce rate, realtime visitors, visitors device, and more.

you should first create an account for google analytics and add a website and it will provide you a token with a script that you should put inside your head tag. In case you are using react it can be handled by `react-helmet` package. Be aware to create a sperate site for `dev` and `production` sites in case you have different environments for development and testing and production. 

#### Google Tag Manager
Here you as a software engineer/frontend developer (since you visit this repo) may ask your self these tools are marketing related and they may ask us to add or change their configs anytime also DevOps and Q/A team gonna involve since in web app you should build another time a release app again for every change. Wouldn't be nice if the marketing team do their job and add third party script that they need for their job. `google tag manager` is a solution for this. you as a developer-only need to implement and insert it on a web app and after that marketing team can use `GTM` to add different scripts and the best part is their change gonna be realtime. 

#### Alexa
Alexa is a website that can help you to know your competitors and also potential keywords. it will show you the rank of your website on all the web (don't worry or get happy this is just an estimation). So your rank gonna depend on your traffic or other traffics.

#### Similarweb
This is site is something like Alexa but it offers some extra info that you can't find on Alexa so checking this site to find your competitors and also find a new solution to improve your site gonna be useful.

#### google search console
Search Console tools and reports help you measure your site's Search traffic and performance, fix issues, and make your site shine in Google Search results

### Google and SPA
Google will try to index website as fast as possible and also can detect SPA websites but since rendering is expensive it will not gonna be indexed like other website with server-side rendering so in many cases you will be ok with only SPA website but in cases that your content is up to date and need to be indexed as fast as possible you need to do some workarounds to server-side render your website so google not put your site to the queue for indexing.
[spa SEO mission impossible?](https://www.magnolia-cms.com/blog/spa-seo-mission-impossible.html)

## SEO insight for your site
You can use google audit which you can find inside devtools of google chrome by opening devtools and chose `audit` tab. it will check your site and help you to fix your SEO errors. Also, there are some other online web sites that you can use to get more suggestions about your website SEO.
- [neilpatel](https://neilpatel.com/seo-analyzer/)
- [SEOCheckup](https://seositecheckup.com/)
- [WooRank](https://www.woorank.com/)

be aware that some. of these websites may not work with SPAs. 

### Canonical
If you have a single page accessible by multiple URLs, or different pages with similar content (for example, a page with both a mobile and a desktop version), Google sees these as duplicate versions of the same page. Google will choose one URL as the canonical version and crawl that, and all other URLs will be considered duplicate URLs and crawled less often. (Resource [google](https://support.google.com/webmasters/answer/139066?hl=en))
There are some ways to specify a canonical page that you can refer to on the provided link.

### SPA Solutions 
Sometime its best to have SSR on your website instead of single page application for SEO, since google will not wait to much for your site to render and it will be in a queue to find time to render them.

### Some practices
Never index search page in case you have search page this may cause black SEO problems and your site have too many pages with no data and mark as a duplicate (canonical may help with this).
Have a 404/not found page.
Do not use too many redirects.

### Hint google for re-crawl
By adding last modified to site map file you can tell google bot that the content of the page has been changed and need re-crawl. Be aware that google bot would evaluate your changes and if the page change would be minor and not worth re-crawling it will understand and won't trust your last modified property anymore so keep that in mind.[resource](https://www.youtube.com/watch?v=am4g0hXAA8Q&t=926s)

### Knowledge panels
Knowledge panels are information boxes that appear on Google when you search for entities (people, places, organizations, things) that are in the Knowledge Graph. They are meant to help you get a quick snapshot of information on a topic based on Google’s understanding of available content on the web.

### Performance vs Releative content
Speed and performance are important but not as much as content. providing more reach content and update it will have more effect than trying to score perfectly on lighthouse or similar websites(TODO: add resource)


### Understand how structured data works
Helps with showing more rich data in google 


## Tips
In case you have SPA and you want to check and see how google crawled your website you can search yor site inside google and click on cache to see your site.

* [submit your content](https://support.google.com/webmasters/answer/6259634)
* [SEO Tools](https://github.com/teles/awesome-seo)
