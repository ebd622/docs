# Java
### Asynchronous Programming in Java: Options to Choose from
* https://youtu.be/1zSF1259s6w?si=xcstf3NZWhn0SNfK

#### Threading
* Parallel vs Concurrent
* Parallel vs Async
* Why not callback (23:40)
  * How to handle callback?
  * There is no standard as whether you get data first of the error first
  * There is no standard as whtat to do if the callback itself were to fail
  * How do you deal with multiple level of nested callback?
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

#### Threads vs Virtual Threads
* Virtual Threads (1:23:20)
* Java21 is most important release of Java (because of VT). VT makes a huge change in Java eco-system!
* Quick demo of VT with Kotlin (subroutine, coroutine, continuations concept) (1:28:25)
  * Continuation is a datastructure that halps to restore the context of a call between calls to a coroutine (1:44:04)
  * Continuation should be a datastructure that you bebefit from but should not have a direct access to it
  * VTs are supper lightweight. They are manages by JVM, not by OS (1:52:30)
  * A carrier thread is a traditional OS thread that is used by the JVM to execute VTs.
  * A VT is mounted and unmounted to a carrier thread (1:53:35)
  * Mounting and unmouting takes some time, it is not free (because it is not possible to get something with absolutely no overhead!) (1:55:00)
  * Quick example (2:07:45)
  * Don't confuse ExecutorService with pooling (2:14:30)
  * No any sense to pool VT (2:15:50)
  * Coninue example with VT (2:18:10)
  * Where it makes sense to use VT? (2:24:45)
  * What to do and what doesn't (2:26:35)

### Project Loom: Modern Scalable Concurrency for the Java Platform
* https://devoxx.be/talk/?id=12201
* https://www.youtube.com/watch?v=XF4XZlPZc_c&t=1s

TODO
