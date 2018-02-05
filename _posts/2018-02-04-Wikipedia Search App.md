---
layout: post
title: Above and Beyond With freeCodeCamp's Wikipedia Search App
---

This week I made a [simple App](https://codepen.io/teebl/full/gvrXEP) as part of the freeCodeCamp course that allows you to search wikipedia, and returns results with images and a short intro to the article. I also took the extra time to add some finishing touches, such as animations and image thumbnails, and a little twist on the random webpage freeCodeCamp suggests making on this project.

This project was really fun. The wiki API has pretty good documentation, although I had a bit of trouble when I found the standard route of `"search": "list"` does not have a method of pulling photos. Here's my finalized JSON request:

```
{
	"action": "query",
	"format": "json",
	"prop": "pageimages|extracts|info",
	"generator": "search",
	"redirects": 1,
	"formatversion": "2",
	"piprop": "thumbnail",
	"pithumbsize": "100",
	"pilimit": "10",
	"exsentences": "2",
	"exintro": 1,
	"inprop": "url",
	"grnnamespace": "0",
	"grnlimit": "10"
}
```
Instead of `"search": "list"`, I found an interesting workaround with the 
`"generator"` request. It allowed me to include props when I searched, which is how I got thumbnails to be included in the response. 

Along with `"prop": "pageimages"` there are a couple other properties I requested. I used the first, `extracts`, to grab the first two sentences of the introduction to the article. Wikipedia custom dictates these will be a straightforward summary of the article. I used that as the description in the results returned.

The second prop, `info` was used to include the url, specified with `"inprop": "url"`. I used it to make the link to the article.

I'll save you the rest, but I think you get the idea.

As for the other touches. I used `append()` to build the unordered list of results, but as default all list items were set to `display: none` in the CSS. This allowed me to `fadeIn()` all the results, one by one (using `each()`).

The cherry on top for this project was when I did some digging and found `"generator: "random"`. freeCodeCamp suggests a random article button for this project, but throws a softball by bluntly suggesting using the link <https://en.wikipedia.org/wiki/Special:Random>.

With `"generator: "random"`, I can make a similar query to the search query above, but instead it would return ten *random* search results. Not a bad addition, eh?

Thanks for stopping by! Feel free to leave any comments on the codepen, I'll have another post up before you know it.



