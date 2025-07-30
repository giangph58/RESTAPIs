# RESTAPIs
Document my learning of REST APIs module of the Python course from University of Michigan

# Projects

This project will take you through the process of mashing up data from two different APIs.  

[The OMDb API](https://www.omdbapi.com/) lets you provide a movie title as a query input and get back data about the movie, including scores from various review sites (Rotten Tomatoes, IMDb, etc.).

[icanhazdadjokes.com](https://icanhazdadjoke.com/) returns random dad jokes containing a search string that you specify in your query.

The end result of this project will be a function that takes in a movie title as input and produces a formatted text string that includes a couple dad jokes related to a word from the movie's plot.

For example, here are a couple of sample outputs:

---

```
Baby Mama
Rotten Tomatoes rating: 63%
A successful, single businesswoman who dreams of having a baby discovers she is infertile and hires a **working** class woman to be her unlikely surrogate.
Speaking of **working**, that reminds me of some jokes.
Hope they're better than the movie!

Want to hear a joke about construction? Nah, I'm still **working** on it.
Why doesn't the Chimney-Sweep call out sick from work? Because he's used to **working** with a flue.
```

---

```
Back to the Future
Rotten Tomatoes rating: 93%
Marty McFly, a 17-year-old high school student, is **accidentally** sent 30 years into the past in a time-traveling DeLorean invented by his close friend, the maverick scientist Doc Brown.
Speaking of **accidentally**, that reminds me of some jokes.
Hope they're as good as the movie!

I **accidentally** drank a bottle of invisible ink. Now I’m in hospital, waiting to be seen.
A butcher **accidentally** backed into his meat grinder and got a little behind in his work that day.
```
---


To avoid problems with rate limits and site accessibility, we have provided a cache file with results for all the queries you need to make to both OMDb and icanhazdadjokes. Just use `requests_with_caching.get()` rather than `requests.get()`. If you're having trouble, you may not be formatting your queries properly, or you may not be asking for data that exists in our cache. We will try to provide as much information as we can to help guide you to form queries for which data exists in the cache.

## ALERT: All Query Results Should Be Found in the Cache File
If you ever run `requests_with_caching.get()` and it says either of the following, then **something was wrong** with your query:
- new; adding to cache
- found in page-specific cache
