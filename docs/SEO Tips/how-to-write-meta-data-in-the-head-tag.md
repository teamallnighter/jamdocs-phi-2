---
title: How to write meta data in the head tag
date: 2020-10-16
slug: metadata-head-tag

---
### General

These are the most commonly used meta tags inside of the head tag. Anything between <!----> are notes and are not picked up by the browser

    <!--
      The following 2 meta tags *must* come first in the <head>
      to consistently ensure proper document rendering.
      Any other head element should come *after* these tags.
    -->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    
    <!--
      Allows control over where resources are loaded from.
      Place as early in the <head> as possible, as the tag  
      only applies to resources that are declared after it.
    -->
    <meta http-equiv="Content-Security-Policy" content="default-src 'self'">
    
    <!-- Name of web application (only should be used if the website is used as an app) -->
    <meta name="application-name" content="Application Name">
    
    <!-- Theme Color for Chrome, Firefox OS and Opera -->
    <meta name="theme-color" content="#4285f4">
    
    <!-- Short description of the document (limit to 150 characters) -->
    <!-- This content *may* be used as a part of search engine results. -->
    <meta name="description" content="A description of the page">
    
    <!-- Control the behavior of search engine crawling and indexing -->
    <meta name="robots" content="index,follow"><!-- All Search Engines -->
    <meta name="googlebot" content="index,follow"><!-- Google Specific -->
    
    <!-- Tells Google not to show the sitelinks search box -->
    <meta name="google" content="nositelinkssearchbox">
    
    <!-- Tells Google not to provide a translation for this document -->
    <meta name="google" content="notranslate">
    
    <!-- Verify website ownership -->
    <meta name="google-site-verification" content="verification_token"><!-- Google Search Console -->
    <meta name="yandex-verification" content="verification_token"><!-- Yandex Webmasters -->
    <meta name="msvalidate.01" content="verification_token"><!-- Bing Webmaster Center -->
    <meta name="alexaVerifyID" content="verification_token"><!-- Alexa Console -->
    <meta name="p:domain_verify" content="code_from_pinterest"><!-- Pinterest Console-->
    <meta name="norton-safeweb-site-verification" content="norton_code"><!-- Norton Safe Web -->
    
    <!-- Identify the software used to build the document (i.e. - WordPress, Dreamweaver) -->
    <meta name="generator" content="program">
    
    <!-- Short description of your document's subject -->
    <meta name="subject" content="your document's subject">
    
    <!-- Gives a general age rating based on the document's content -->
    <meta name="rating" content="General">
    
    <!-- Allows control over how referrer information is passed -->
    <meta name="referrer" content="no-referrer">
    
    <!-- Disable automatic detection and formatting of possible phone numbers -->
    <meta name="format-detection" content="telephone=no">
    
    <!-- Completely opt out of DNS prefetching by setting to "off" -->
    <meta http-equiv="x-dns-prefetch-control" content="off">
    
    <!-- Specifies the document to appear in a specific frame -->
    <meta http-equiv="Window-Target" content="_value">
    
    <!-- Geo tags -->
    <meta name="ICBM" content="latitude, longitude">
    <meta name="geo.position" content="latitude;longitude">
    <meta name="geo.region" content="country[-state]"><!-- Country code (ISO 3166-1): mandatory, state code (ISO 3166-2): optional; eg. content="US" / content="US-NY" -->
    <meta name="geo.placename" content="city/town"><!-- eg. content="New York City" -->

### Facebook Open Graph

If someone shares your page to facebook, facebook will use this meta data about your site.

    <meta property="fb:app_id" content="123456789">
    <meta property="og:url" content="https://example.com/page.html">
    <meta property="og:type" content="website">
    <meta property="og:title" content="Content Title">
    <meta property="og:image" content="https://example.com/image.jpg">
    <meta property="og:image:alt" content="A description of what is in the image (not a caption)">
    <meta property="og:description" content="Description Here">
    <meta property="og:site_name" content="Site Name">
    <meta property="og:locale" content="en_US">
    <meta property="article:author" content="">

### Twitter Card

If someone shares your web site or blog post on twitter this meta data is used

    <meta name="twitter:card" content="summary">
    <meta name="twitter:site" content="@site_account">
    <meta name="twitter:creator" content="@individual_account">
    <meta name="twitter:url" content="https://example.com/page.html">
    <meta name="twitter:title" content="Content Title">
    <meta name="twitter:description" content="Content description less than 200 characters">
    <meta name="twitter:image" content="https://example.com/image.jpg">
    <meta name="twitter:image:alt" content="A text description of the image conveying the essential nature of an image to users who are visually impaired. Maximum 420 characters.">

### IOS

    <!-- Smart App Banner -->
    <meta name="apple-itunes-app" content="app-id=APP_ID,affiliate-data=AFFILIATE_ID,app-argument=SOME_TEXT">
    
    <!-- Disable automatic detection and formatting of possible phone numbers -->
    <meta name="format-detection" content="telephone=no">
    
    <!-- Launch Icon (180x180px or larger) -->
    <link rel="apple-touch-icon" href="/path/to/apple-touch-icon.png">
    
    <!-- Launch Screen Image -->
    <link rel="apple-touch-startup-image" href="/path/to/launch.png">
    
    <!-- Launch Icon Title -->
    <meta name="apple-mobile-web-app-title" content="App Title">
    
    <!-- Enable standalone (full-screen) mode -->
    <meta name="apple-mobile-web-app-capable" content="yes">
    
    <!-- Status bar appearance (has no effect unless standalone mode is enabled) -->
    <meta name="apple-mobile-web-app-status-bar-style" content="black">
    
    <!-- iOS app deep linking -->
    <meta name="apple-itunes-app" content="app-id=APP-ID, app-argument=http/url-sample.com">
    <link rel="alternate" href="ios-app://APP-ID/http/url-sample.com">

### Android

    <meta name="theme-color" content="#E64545">
    
    <!-- Add to home screen -->
    <meta name="mobile-web-app-capable" content="yes">
    <!-- More info: https://developer.chrome.com/multidevice/android/installtohomescreen -->
    
    <!-- Android app deep linking -->
    <meta name="google-play-app" content="app-id=package-name">
    <link rel="alternate" href="android-app://package-name/http/url-sample.com">

### Google Chrome

    <link rel="chrome-webstore-item" href="https://chrome.google.com/webstore/detail/APP_ID">
    
    <!-- Disable translation prompt -->
    <meta name="google" content="notranslate">