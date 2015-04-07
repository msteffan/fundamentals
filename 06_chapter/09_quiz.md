**WDI Fundamentals Unit 6**

Read the following code and then answer the questions below.

```js
var loginInfo = {"username": "johnny23", "password": "hunter2"};
```
---

Given the above code, how would you access 'hunter2'?

- [ ] `loginInfo["hunter2"]`
- [ ] `loginInfo("hunter2")`
- [x] `loginInfo["password"]`
- [ ] `loginInfo("password")`

> Not quite.
> To access the value associated with the key password you would need to use
> the command: loginInfo["password"]

Given the above code, how would you change the username to "billy96?"

- [ ] `login_info("username") = "billy96"`
- [x] `login_info["username"] = "billy96"`
- [ ] `login_info["username", "billy96"]`
- [ ] `login_info("username", "billy96")`

> Not quite.
> You modify an associative array in much the same way you would a regular array.
> Instead of referring to the element by the index, you would specify the key
> value of the element you'd like to change.
> In this example, you would write:
> `login_info["username"] = "billy96"`

---

Read the following code and answer the questions below.

```js
var twitterAccount = {
  userName: 'wilw',
  followers: [
    'gates_mcfadden',
    'jonathanfrakes',
    'SirPatSew',
    'akaworf'
  ],
  following: [
    'wesleytips',
    'RikerGoogling'
  ],
  tweets: [
    {
      body: 'The Vampire who liked having a cold because he was really into his coffin',
      retweets: 207,
      favorites: 528
    },
    {
      body: 'I am mixing #RadioFreeBurrito episode 40',
      retweets: 12,
      favorites: 92
    },
    {
      body: 'Based on my very small sample size in this Starbucks, mom jeans are making a comback with twenty-somethings',
      retweets: 102,
      favorites: 480
    }
  ],
}
```

{% exercise %}
How would you access or drill down inside a large data structure?
Declare a variable `followers` and assign it to the array of the accounts that wilw follows.
{% initial %}
// var followers;
{% solution %}
var followers = twitterAccount.followers;
{% validation %}
assert(followers == twitterAccount.followers);
{% context %}
var twitterAccount = {
  userName: 'wilw',
  followers: [
    'gates_mcfadden',
    'jonathanfrakes',
    'SirPatSew',
    'akaworf'
  ],
  following: [
    'wesleytips',
    'RikerGoogling'
  ],
  tweets: [
    {
      body: 'The Vampire who liked having a cold because he was really into his coffin',
      retweets: 207,
      favorites: 528
    },
    {
      body: 'I am mixing #RadioFreeBurrito episode 40',
      retweets: 12,
      favorites: 92
    },
    {
      body: 'Based on my very small sample size in this Starbucks, mom jeans are making a comback with twenty-somethings',
      retweets: 102,
      favorites: 480
    }
  ],
}
var followers;
{% endexercise %}

{% exercise %}
How would you access or drill down inside a large data structure?
Declare a variable `firstTweetBody` and assign it to the body of the first tweet.
{% initial %}
// var firstTweetBody;
{% solution %}
var firstTweetBody = twitterAccount.tweets[0].body;
{% validation %}
assert(firstTweetBody == twitterAccount.tweets[0].body);
{% context %}
var twitterAccount = {
  userName: 'wilw',
  followers: [
    'gates_mcfadden',
    'jonathanfrakes',
    'SirPatSew',
    'akaworf'
  ],
  following: [
    'wesleytips',
    'RikerGoogling'
  ],
  tweets: [
    {
      body: 'The Vampire who liked having a cold because he was really into his coffin',
      retweets: 207,
      favorites: 528
    },
    {
      body: 'I am mixing #RadioFreeBurrito episode 40',
      retweets: 12,
      favorites: 92
    },
    {
      body: 'Based on my very small sample size in this Starbucks, mom jeans are making a comback with twenty-somethings',
      retweets: 102,
      favorites: 480
    }
  ],
}
var firstTweetBody;
{% endexercise %}

{% exercise %}
How would you access or drill down inside a large data structure?
Declare a variable `totalTweets` and assign it to the total number of tweets
that have been made by wilw so far?
{% initial %}
// var totalTweets;
{% solution %}
var totalTweets = twitterAccount.tweets.length;
{% validation %}
assert(totalTweets == twitterAccount.tweets.length);
{% context %}
var twitterAccount = {
  userName: 'wilw',
  followers: [
    'gates_mcfadden',
    'jonathanfrakes',
    'SirPatSew',
    'akaworf'
  ],
  following: [
    'wesleytips',
    'RikerGoogling'
  ],
  tweets: [
    {
      body: 'The Vampire who liked having a cold because he was really into his coffin',
      retweets: 207,
      favorites: 528
    },
    {
      body: 'I am mixing #RadioFreeBurrito episode 40',
      retweets: 12,
      favorites: 92
    },
    {
      body: 'Based on my very small sample size in this Starbucks, mom jeans are making a comback with twenty-somethings',
      retweets: 102,
      favorites: 480
    }
  ],
}
var totalTweets;
{% endexercise %}

[One last exercise - this time on associative arrays.](10_exercise.md)
