
# VK API

We have already discussed how you can download and process information from any web page. In addition to this capability, some services provide an application programming interfrace (API). The API allows you to access the service directly and receive ready-made data in a structured form.

VKontakte also has an API with fairly detailed [documentation](https://vk.com/dev.php?method=manuals).

For example, [here](https://vk.com/dev/methods) is a list of all API methods. And [here](https://vk.com/dev/users) you can see a list of methods associated with users. API methods are intended primarily for application development, this should be taken into account when reading the description of the methods.  Among the user methods, we are interested in obtaining [information about users](https://vk.com/dev/users.get), as well as [searching for users](https://vk.com/dev/users.search) that meet the given criteria. If you are logged in on VKontakte, then you can immediately see how the methods work on the site. 

API methods can be called from your own scripts, this allows you to automatically collect and process information from VKontakte. API calls require token. There are several types of tokens you could pass.

To receive the token we have to request it first. To begin with, the application should be registere on ***vk.com****. Then we construct the valid request using **`client_id`**, **`redirect_uri`** and **`score`**. Here we choose **`response_type=token`**. You can click on the link to receive your own token

see [vk_api examples](https://github.com/python273/vk_api)

* [VK auth starter](https://colab.research.google.com/drive/1gYtd9hqwRub7S5u4f7Ku_qPAR_dBg0Jv?usp=sharing)
* [VK group analysis](https://colab.research.google.com/drive/1Hmf66p0UZDtuUY2PKQPi6Rf01XnbjCbE?usp=sharing)
* [VK friend network analysis](https://colab.research.google.com/drive/1tUNrce1T_8zsIWfLlNLaiOSGYI0bMBhi?usp=sharing)
* [VK Auth (unstable)](https://colab.research.google.com/drive/1CtFn1jVKWssP1Jf_c1P-mMgYOu4RWh_Z?usp=sharing)
* [VK Scraping (Bots)](https://colab.research.google.com/drive/1g8LduMGH3wv3cy2n5T3jWi1hiebMVBJg?usp=sharing)


## Facebook 
[Facebook scraping guide](https://colab.research.google.com/drive/1OU1l5EvbkpJap6RdyBA5W_O8uPMzJyyt?usp=sharing)


You also can find similar guidelines for [Facebook](http://nbviewer.ipython.org/github/chdoig/Mining-the-Social-Web-2nd-Edition/blob/master/ipynb/Chapter%202%20-%20Mining%20Facebook.ipynb) and [Twitter](http://mark-kay.net/2014/08/15/network-graph-of-twitter-followers/) APIs