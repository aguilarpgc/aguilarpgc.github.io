---
layout: post
title:  "PGCTextView"
date:   2018-05-03 15:34:12 -0500
---

I've released a small library that works on UIKit: A UITextView subclass which you can customize some UI and logic aspects for two elements: A placeholder and a counter label.

The properties can also be changed throught the Identity Inspector in the xib file.


# Placeholder
The below properties affects the placeholder label: Color, font and text.

{% highlight swift %}
textView.placeholderColor = .darkGray
textView.placeholderFont = UIFont.italicSystemFont(ofSize: 25)
textView.placeholderText = "Placeholder"
{% endhighlight %}

# Counter

First, you can change some UI aspects like color and font for the counter label. This counter will show the amount of characters that is currently in the UITextView or it will show the remaining characters that the user can type (depending on `isCounterAscending` and `maxCharacters`).

{% highlight swift %}
textView.counterColor = .blue
textView.counterFont = UIFont.italicSystemFont(ofSize: 11)
textView.isCounterAscending = true
textView.isCounterVisible = true
textView.maxCharacters = 50
{% endhighlight %}

`maxCharacters`: Number of characters that the user can type.

`isCounterAscending`: If `true`, then the counter will count from 0 to `maxCharacters`. Or it will count from `maxCharacters` to 0 if `false`.

`isCounterVisible`: You can hide the counter label if you want to.


# Project
Here's the project in [Github](https://github.com/aguilarpgc/PGCTextView).
