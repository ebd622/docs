# Data&AI
Talks:
* By session types: https://devoxx.be/2023-schedule/talks-by-sessions/
* By tracks: https://devoxx.be/2023-schedule/talks-by-tracks/

## Data & AI
#### JetBrains AI: A Deep Dive
* https://devoxx.be/talk/?id=70102
* https://www.youtube.com/watch?v=MYhkTnag81o&t=1524s

## Java
#### Asynchronous Programming in Java: Options to Choose from
* https://devoxx.be/talk/?id=64003
* https://youtu.be/1zSF1259s6w?si=xcstf3NZWhn0SNfK

##### Threading
* Parallel vs Concurrent
* Parallel vs Async
* Why not callback (23:40)
  * How to handle callback?
  * There is no standard as whether you get data first of the error first
  * There is no standard as whtat to do if the callback itself were to fail
  * How to you deal with multiple level of nested callback?
  * Code becomes horrible
* Concept of Promises of JavaScript (25:20)
* CompletableFuture in Java is Promises in JavaScript (42:20)
* CompletableFuture can be in 3 states (the same like Promises): (46:23)
  * Pending
  * Resolved
  * Rejected
* Stream API vs CompletableFeature API (56:00)
* Heandle exceptions in CompletableFeature (1:06:30)
* Fail on timeout (1:13:20)
* Combine and Compose (1:14:00)

##### Threads vs Virtual Threads
* Virtual Threads (1:23:20)
* Java21 is most important release of Java (because of VT). VT makes a huge change in Java eco-system!
* Quick demo of VT with Kotlin (subroutine, coroutine, continuations concept) (1:28:25)
  * Continuation is a datastructure that halps to restore the context of a call between calls to a coroutine (1:44:04)
  * Continuation should be a datastructure that you bebefit from but should not have a direct access to it
  * VTs are supper lightweight. They are manages by JVM, not by OS (1:52:30)
  * There is a carrier thread and VT is mounted and unmounted to a carrier thread (1:53:35)
  * Mounting and unmouting takes some time, it is not free (because it is not possible to get something with absolutely no overhead!) (1:55:00)
  * Quick example (2:07:45)
  * Don't confuse ExecutorService with pooling (2:14:30)
  * No any sense to pool VT (2:15:50)
  * Coninue example with VT (2:18:10)
  * Where it makes sense to use VT? (2:24:45)
  * What to do and what doesn't (2:26:35)

#### With Java 21, Your Code Runs Even Faster. But How is that Possible?
* https://devoxx.be/talk/?id=4454
* https://www.youtube.com/watch?v=T6X2Yytrzyg&t=682s

  

## Server Side Java
#### Spring Infrastructure Deep Dive: Virtual Threads, Checkpoint Restore, Native Images
* https://devoxx.be/talk/?id=20285
* https://www.youtube.com/watch?v=YfFYTR8_lBY
##### The impact of virtual threads
  * Two incarnations of thread (5:50):
    * Platform therad (`PT`) - traditional operating system thread
    * Virtual thread (`VT`)
  * VT is attacted to PT whenever it performs work
  * VT has abitilty to detach itelf from a PT whenever it hits a blocking point (so, it is never blocks a platfoem thread)
  * Whenever a blocking conditions is being released, a VT is reatached to PT again
  * The most important aspect of adopting VT in a Spting stack is the server container setup (8:57)
  * Traditional Spring MVC setup (on either Tomcat or Jetty) runs withing a thread pool managed by a server container:
    *  Server container has an HTTP connector;
    *  A connector has an executor attached
    *  Whenever a request comes in, it dispatches a servlet thread to Spring MVC's dispatcher servlet and Spring takes it from there.

##### Deep dive: Spring's runtime efficiency theme

##### Deep dive: Spring's cleint-side HTTP support (1:20:10)
* RestTemplate intorduction 15 years ago: Upsides and Downsides (1:22:15)
* WebClient introduced in Spring5 (1:27:00)
* VT (1:29:15)
  * Spring Framework 6.1 sipports VT
  * Spring Boot 3.2 offers a property `spring.threads.virtual.enabled`. Setting it to `true` will enable VT for Tomcat&Jetty. (cleint applications will be running on VTs)
* Use WebClient instead of RestTemplate? (1:34:00)
* Demo and samples (https://github.com/poutsma/restclient-sample) (1:35:36)
  * Use Parameeterized Types (1:49:11)
  * Error Handling (1:53:48)
  * Exchange method (1:57:40)
  * ClientRequestFactories (2:01:22)
