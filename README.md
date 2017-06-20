## Memoizing and Caching

### Memoizing in Ruby 

To improve performance we can rely on previously computed values instead of recomputing them.  This is called memoization.  When we memoize, we save the time needed to recalculate them, but our answer may not be up to date.

* [Memoize in Ruby](http://gavinmiller.io/2013/basics-of-ruby-memoization/)

### SQL Caching

Activerecord will provide caching for you out of the box.  Caching is when instead of computing a value twice, the program simply references the result of the first computation.

For activerecord, if you search for `Author.all` or any query multiple times on a request, activerecord will not query the database multiple times.  Instead, it references the already completed query.

You can read more about how database caching works with Rails here: 
[SQL Caching](http://guides.rubyonrails.org/caching_with_rails.html#sql-caching)

	
### Caching Queries

While activerecord will cache queries made in the same request for you automatically, sometimes you may want to retrieve queries from the cache the first time the query is made in a cache.  To achieve something like this, we can lean on the memcache store in Rails.  Take a look at the benefits of using the memcache store, and how to set it up by looking at the following resources: 

First watch the first few minutes of the below video which discusses Redis.  Redis is a separate database, that works similarly to how memcache (or caching in memory) works in Rails.  You can stop after a few minutes, when the video moves onto talking about pubsub with Redis, that is a separate topic.  

* [Redis Video](https://www.youtube.com/watch?v=OeVHnyztV9A)

The author of the video does an excellent job explaining the use case for using a tool, or Rails:Memcached.  After watching the video, move on to how to use the MemCache tool available with Rails.

* [Railscast on Memcached](https://www.youtube.com/watch?v=eO8tTPDEB8A&t=1s) 
* [Memcached on Heroku](https://devcenter.heroku.com/articles/building-a-rails-3-application-with-memcache)
* [Rails Memcached Blog Entry](http://vinsol.com/blog/2014/02/11/guide-to-caching-in-rails-using-memcache/)
<p class='util--hide'>View <a href='https://learn.co/lessons/ruby-and-model-performance'>Ruby and Model Performance</a> on Learn.co and start learning to code for free.</p>
