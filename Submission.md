Edit this page to describe your Submission.

## Which Categories Best Fit Your Submission and Why?

In order of what I think fits my contributions best (best fit first). 

This will be a bit murky as the categories are not 
defined in much detail anywhere. My contributions are to an API and its implementation, so a lot
of these categories overlap, imho (API usability, API portability and API quality are quite strongly
correlated, if you ask me).

So take your pick below...

* Best new feature

  I added lots of new features to RxJava, mostly in the form of many **new operators**, but also
  by improving on **schedulers** and **generics**.

* Best contribution to code quality

  I cleaned up a lot of warnings in the RxJava project. I helped make it a lot more **typesafe**.
  I added **co-/contravariance** which could be considered an API quality improvement. I wrote a 
  lot of **tests against RxJava features**. I created and implemented an RxJava **[scheduler 
  specifically for testing](https://github.com/Netflix/RxJava/blob/master/rxjava-core/src/main/java/rx/concurrency/TestScheduler.java)** 
  behavior of scheduled actions.

* Best portability enhancement

  By contributing to making RxJava more **typesafe** and more **generic**, and by contributing 
  to the discussions about Scala integration, I helped make RxJava more portable to other 
  (typesafe) programming languages like Java, Scala and Kotlin.
  
  Also, the whole RxJava project foundation is about **porting Rx.NET functionality** over to 
  the JVM world.

* Best usability enhancement

  As RxJava is an API, this is about API usability. I think I contributed a lot to API usability
  by making the API more **typesafe** and introducing **co- and contravariance** everywhere.

## Describe your Submission

### Motivation

I stumbled upon RxJava in March when looking for Rx for the JVM (for Scala, to be more specific). 
I was trying to write a little Android game in Scala and got lost in callback hell quickly - 
so I was looking for a way out via Rx.

Even at that time, RxJava looked very promising. However, it was not only missing features that I needed,
but it also turned out to be implemented in a not very typesafe way (a lot of raw types and objects).
This was due to being mostly used from dynamic languages at Netflix, of course, but it hurt a lot when 
used from Scala.

So I decided to improve all that, and thanks to a very friendly, quick and "reactive" Ben Christiansen,
I was on board quickly.

### Goals

My personal goals while contributing were the following, in order of importance to me:

* Help make the library typesafe and clean it up a bit
* Help add features, mostly those that I was missing in order to create a simple Swing demo 
  (inspired by [Pong in Elm](http://elm-lang.org/blog/games-in-elm/part-0/Making-Pong.html))
* Help add schedulers to make concurrency work well
* Help make RxJava more popular
* Help improve integration with Scala
* Help improve Android support

### Contributions

With the exception of the last goal from above, my contributions helped achieve these goals, 
in my honest opinion.
Of course I wasn't doing all this alone. I have to thank Ben and many others for a lot 
of help here.

My first contribution was starting a 
**[discussion about typesafety](https://groups.google.com/forum/#!topic/rxjava/bVZoKSsb1-o)** 
in the RxJava Google Group. This developed into a large reworking of the RxJava core to make
it a lot more typesafe. I haven't contributed much to the reworking itself as other people were
way better qualified to do this; however, I got the ball rolling here.

Then, I added a lot of features to RxJava in the form of **implementations of Rx operators**, helped
with the **Rx schedulers** and added a module for **Swing integration**.

All in all, I added the following operators to RxJava (up to now):

* `average`
* `combineLatest`
* `count`
* `delay`
* `distinct`
* `distinctUntilChanged`
* `first`
* `firstOrDefault`
* `interval`
* `mapWithIndex`
* `sample`
* `skipWhile`
* `skipWhileWithIndex`
* `sum`
* `timestamp`

In my own view, my **main contribution** was the large rework of the codebase to generalize the types to become **covariant** (observables, function return types and a few small other types) or
**contravariant** (observers and function parameter types) where possible. This is an important
cornerstone for improving **Scala integration**, too.

I haven't contributed code to the Scala integration because this was taken up by the people from 
[Typesafe](http://typesafe.com) themselves. However, I keep contributing to the 
**[respective discussions](https://github.com/Netflix/RxJava/issues/336)**.

I haven't gotten started yet with Android support, but thankfully, in the meantime, the people from SoundCloud have.

I also recently **held a talk** about RxJava at [Herbstcampus 2013](http://herbstcampus.de/hc13/program/sessions.html#55) (in Nuremberg). 
The (German) **slides and sample code** for this talk can be found at my 
[Github repo "rxjava-samples"](https://github.com/jmhofer/rxjava-samples).

So, that's all there is to this submission: A few contributions to improve RxJava. However, I'm very
proud that [Erik Meijer likes them](https://twitter.com/headinthebox/status/374065370560069632).

## Provide Links to Github Repos for your Submission

* [Netflix/RxJava](https://github.com/Netflix/RxJava) - the Netflix RxJava master repo
* [jmhofer/RxJava](https://github.com/jmhofer/RxJava) - my RxJava fork
* [jmhofer/rxjava-samples](https://github.com/jmhofer/rxjava-samples) - a simple sample application I used for a talk on RxJava
