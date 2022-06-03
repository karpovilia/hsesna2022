Let's log in to the facebook account first

![](https://dl.dropboxusercontent.com/s/jq26657jg4uorbe/fb01.png)

Here we see logged user newsfeed. Let's have a look at the requests panel

![](https://dl.dropboxusercontent.com/s/3nb1a481mh6uxxg/fb02.png)

We can see that frontend requests graphql. Let's copy this request and explore it in Postman.
To do it, create new request and Import your cURL as Waw text

![](https://dl.dropboxusercontent.com/s/i8v4bc05y11lcmh/fb03.png)

As you can see, the response returns json with news feed data. You can quickly format your JSON structure with [online json parser](http://json.parser.online.fr/beta/)

![](https://dl.dropboxusercontent.com/s/23a0zvd7atubdrl/fb04.png)

This text is called Unicode escape sequence, you can use [dencode](https://dencode.com/ru/string/unicode-escape) to decode it.

![](https://dl.dropboxusercontent.com/s/cnlg51oqjbw651k/fb05.png)

Let's find out how frontend gets data from backend. To do it, let's clear Network panel 

![](https://dl.dropboxusercontent.com/s/3cakaahjr6x91xb/fb06.png)

And scroll down to see what requests will arrive at the network panel.
Look!. We found another one graphql request!

![](https://dl.dropboxusercontent.com/s/u9z19d1pq21r9nd/fb07.png)


Let's explore it in Postman too.

![](https://dl.dropboxusercontent.com/s/kzbmzs408i6pikq/fb08.png)


The text decodes to 
```
Psychiatric hospital on March 8st. 
```

As you can see, there is exactly the same text at the frontend page.

![](https://dl.dropboxusercontent.com/s/7g1xfsyb76tokaw/fb09.png)

Now let's take a look at the reuqest structure: In the `Body` Tab of the second request we can find the following `variable`

```
"cursor":"FSIVAhsBXAIVIhhcTVRZek5qVTFNVFEzTVRveE5qTTJOVFV4TkRjeE9qRTNPamc0TkRJeU1qVTVNREE0TlRRd056UTBOekk2TURvdE56UTBNRFk1TWpZMk9Ea3dORGs0TXprME13PT0AGwNVAiIUEAoYAA=="
```

If we spend some time, we will find that facebook (and many onther web pages with "infinite" news feed) has a special token, that gives you an opportunity to request the next "page" of data.

![](https://dl.dropboxusercontent.com/s/iurc81zpke2l67u/fb10.png)

As you can see, the same string is inside the previous response. So, all you need to do to get next list of posts is just extract the cursor from the previous response and put it to the variables of the next request

![](https://dl.dropboxusercontent.com/s/z5im7aiy1deyfhb/fb11.png)

