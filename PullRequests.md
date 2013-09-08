Update this page to describe and link to pull requests made against other NetflixOSS related projects.

## Feature Related Pull Requests

* [RxJava - Implemented the `combineLatest` operator](https://github.com/Netflix/RxJava/pull/207)
  
  This pull request implemented the Rx `combineLatest` operator. 

  Before, it was non-functional code copied from some other operator. 
  I also documented the api and wrote tests to ensure correct behaviour, of course.

  Concurrency-wise, this operator implementation was quite hairy.

* [RxJava - Implemented the `interval` operator](https://github.com/Netflix/RxJava/pull/228)
  
  This pull request implemented the Rx `interval` operator. It was one of the first operators 
  using the new schedulers. While doing this, I noticed that the RxJava schedulers are still
  missing a crucial feature: The capability to schedule actions periodically.
  
  Which lead me to work on the schedulers some more...
  
* [RxJava - Improving schedulers](https://github.com/Netflix/RxJava/pull/229)

  This pull request added a few more methods to the scheduler interface to allow the
  user to propagate state through the scheduled actions. This was merged manually by Ben
  with [PR 235](https://github.com/Netflix/RxJava/pull/235).
  
* [RxJava - Scheduling actions periodically](https://github.com/Netflix/RxJava/pull/246)

  Finally, this pull request adds the one scheduler feature I was still missing. This was quite 
  hairy due to concurrency and recursiveness.
  
* [RxJava - Implemented the `sample` operator](https://github.com/Netflix/RxJava/pull/248)

  Now that the schedulers were in place, I was able to implement sampling at last. After 
  `combineLatest`, this was the next operator I was missing in my simple Swing Pong sample game.
  
* [RxJava - Implemented the `timestamp` operator](https://github.com/Netflix/RxJava/pull/249)

  This was an easy target now that everything else was in place, so I implemented this too.
  
* [RxJava - Swing Scheduler](https://github.com/Netflix/RxJava/pull/254)

  From my Pong sample game, I had a scheduler implementation specific to Swing which I wanted to
  contribute to RxJava. As this is not core RxJava functionality, this pull request led to my 
  establishing the first of currently two "contrib" subprojects of RxJava (the other being the
  Android subproject). 
  
* [RxJava - Adding a few basic observables to the Swing modul](https://github.com/Netflix/RxJava/pull/262)

  This adds a few basic observables to the Swing module (keyboard and mouse events).  

* [RxJava - Adding component events to the Swing module](https://github.com/Netflix/RxJava/pull/265)

  This adds component event observables to the Swing module (component events).  

* [RxJava - Multicasting](https://github.com/Netflix/RxJava/pull/261)
  
  Funnily, I did this at the same time as Ben, so this didn't get merged in...
  
* [RxJava - Adding co- and contravariance](https://github.com/Netflix/RxJava/pull/331)

  This allows for a lot better usage of the RxJava API in typesafe languages (in this case, mostly 
  Java and Scala). This pull request really was a lot of work. Unfortunately, co- and contravariance 
  in Java is difficult and verbose.

* [RxJava - Implementing the `count`, `sum` and `average` operators](https://github.com/Netflix/RxJava/pull/354)

  This pull request implements a few low-hanging fruit (since `reduce` is already in place and
  can be used for these operators) in order to get the number of open issues in RxJava a bit lower.
  
* [RxJava - Implementing the `skipWhile` and `skipWhileWithIndex` operators](https://github.com/Netflix/RxJava/pull/355)

  This pull request addresses two more operators that are quite important for RxJava users imho.
 
## Quality Related Pull Requests

* [RxJava - Implemented the `combineLatest` operator](https://github.com/Netflix/RxJava/pull/207)

  See above. This added a feature, but also cleaned up the suboptimal code that had been pasted
  into the earlier (non-functional) version of the `combineLatest` operator.

* [RxJava - Javadoc and code cleanup](https://github.com/Netflix/RxJava/pull/255)

  The Gradle build output contained too many warnings. My tolerance for warnings is extremely low.
  So I fixed all I could with this pull request.
  
* [RxJava - Improved `scan`, `reduce`, `aggregate`](https://github.com/Netflix/RxJava/pull/257)

  Those implementations were not as general as they could have been, so I improved on them.
  
* [RxJava - Fighting Gradle deprecation warnings](https://github.com/Netflix/RxJava/pull/305)

  Gradle was updated... lots of deprecation warnings were introduced. Now I don't know much about
  Gradle, but I fixed what I could.
  
* [RxJava - Inner classes build fix](https://github.com/benjchristensen/RxJava/pull/1)

  This was just a small build fix on a pull request by Ben and Matt, concerning Scala integration.
  Got merged manually later on.
  
* [RxJava - Reactivating unit tests and re-introducing some lost methods](https://github.com/benjchristensen/RxJava/pull/2)

  Ben was fighting with making the RxJava core typesafe here, I helped a little.
  
* [RxJava - Adding co- and contravariance](https://github.com/Netflix/RxJava/pull/331)

  See above. In my opinion, this is a huge boost in API quality, even if it's quite verbose and 
  ugly in Java.
  
* [RxJava - A little Swing module wrap-up](https://github.com/Netflix/RxJava/pull/350)

  This pull request consists of a few little things that improve the Swing module.
  
## Performance Related Pull Requests

* [RxJava - Improve synchronization of `combineLatest`](https://github.com/Netflix/RxJava/pull/267)

  Here I tried to reduce the amount of synchronization required in the `combineLatest` operator 
  to an absolute minimum in order to improve concurrency.
