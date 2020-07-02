* Database views and scenic gem (https://github.com/scenic-views/scenic)
* Stackprof for benchmarking (--sort-total)
* Tell Don't Ask (are we doing something to the same object with the query result)
* [false].any? -> false (https://twitter.com/thegedge/status/1263211796665679873)
* if you want to bind etc/hosts to your rails server, you need to start your rails server with `rails s -b 127.0.0.1 -p 80` 
* locale is `language[_territory]` and territory is optional e.g. `en_US`
* `delegate_missing_to`
* Base58: 
  * https://github.com/rails/rails/blob/master/activesupport/lib/active_support/core_ext/securerandom.rb
  * https://learnmeabitcoin.com/guide/base58
* https://github.com/rails/rails/blob/master/activesupport/lib/active_support/benchmarkable.rb
* Avoid usage of "violates" or any kind of wording that suggest there are unbreakable rules that we must always follow.
* Use enum instead of boolean in your API (mobile: true vs category: mobile)
* signed ids https://github.com/rails/rails/pull/39313/files
* Interactive mode https://github.com/rails/rails/pull/39444
* Where with block https://github.com/rails/rails/pull/39445
* https://geemus.gitbooks.io/http-api-design/content/en/requests/accept-serialized-json-in-request-bodies.html
* https://github.com/thoughtbot/guides/tree/master/best-practices#testing
* Naming associations

This is a bit subtle, but when I think about this, I think of a "muted notification" as a _notification that has been muted_.

Here, however, we are talking about _the act of muting a notification_.

Although "mute" is a tricky word, I would therefore be tempted to name this `muting`.

Similar examples:

```rb
### Bad
User -> RecommendedRecipe -> Recipe
User -> LikedRecipe -> Recipe

### Good
User -> RecipeRecommendation -> Recipe
User -> Like -> Recipe
```

It often reveal itself in ways like:

```rb
recommended_recipe.recipe # hum? I thought I already _had_ a recipe
```

