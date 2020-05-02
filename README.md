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

- [ ] make your site fast. this can help with your ranking and conversion rate of your business. some fast ways and easy wins to make your site faster are listed below:

1 - use CDN to deliver your site according to user location

2 - optimization of image size and format. try to use image size that match on design. for example card with 250x100 should not have image with original size of 1000x400. also in case of not using transpaernt image try to use jpeg files. there are some sites that you can use for image optimization such as [tinypng](https://tinypng.com/) and [sqoosh](https://squoosh.app/) there are too many things to do but this seems enough for this part

3 - use cache header to make second visit faster

4 - minify and remove unused js or css. here you can use webpack or postcss in case you are working with latest techs of frontend or simply use [minifier](https://www.minifier.org/)

5 - use [AMP](https://developers.google.com/amp). with amp your page gonna serve directly from google and really fast there are some pros and cons and we may cover it later on it own section

### Use open graph
This protocol has been proposed by facebook. This protocol helps with sharing web site links in social media. this way any link that will share on twitter, whatsapp and other platform gonna have title, description or images.

### Tools
So after implementing all or some of earlier suggestion you need to monitor your visit and gather data to see if they are effective or is there something else you need to do to achive better result. 

#### Google analytics
This tools is must have on all website and web apps. you can see user flow and also see all visit to your website. it provides all sorts of informations such as uniqe user visits, bounse rate, realtime visitors, visitors device and more.

you should first create an account for google analytics and add a website and it will provide you a token with a script that you should put inside your head tag. In case you are using react it can be handled by `react-helmet` package. Be aware to create sperate site for `dev` and `production` sites in case you have differant enviroments for development and testing and production. 

### Google Tag Manager
Here you as a software engineer / frotend developer (since you visit this repo) may ask your self these tools are marketing related and they may ask us to add or change their configs anytime also DevOps and Q/A team gonna involve since in web app you should build another time an release app again for every change. Wouldn't be nice if marketing team do their job and add third party script that they need for their job. `google tag manager` is a solution for this. you as a developer only need to implement and insert it on a web app and after that marketing team can use `GTM` to add differant scripts and the best part is their change gonna be realtime. 

