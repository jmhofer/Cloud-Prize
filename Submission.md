Edit this page to describe your Submission.

## Which Categories Best Fit Your Submission and Why?

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
* Help improve integration with Scala
* Help improve Android support

### Contributions

With the exception of the last goal from above, my contributions achieved these goals, in my honest opinion.
Of course I wasn't doing all this alone. I have to thank Ben again for a lot of help here.

> **TODO** Point to google group discussion re typesafety here!

In my own view, the main contribution was the large rework of the codebase to generalize the types to become covariant (observables, function return types and a few small other types) or contravariant (observers and function parameter types) where possible. This is an important cornerstone for improving Scala integration, too.

I haven't contributed code to Scala integration because this was taken up by the people from Typesafe themselves. However, I keep contributing to the respective discussions.

I haven't gotten started yet with Android support, but thankfully in the meantime, the people from SoundCloud have.

So, that's all there is to this submission: A few contributions to improve RxJava.

## Provide Links to Github Repo's for your Submission

* [RxJava](https://github.com/jmhofer/RxJava) - my RxJava fork
* [rxjava-samples](https://github.com/jmhofer/rxjava-samples) - a simple sample application I used for a talk on RxJava
