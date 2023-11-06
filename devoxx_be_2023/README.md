# Devoxx Belgium 2023
Talks:
* By session types: https://devoxx.be/2023-schedule/talks-by-sessions/
* By tracks: https://devoxx.be/2023-schedule/talks-by-tracks/

## Data & AI
[JetBrains AI: A Deep Dive](https://www.youtube.com/watch?v=MYhkTnag81o&t=1524s)

## Java
#### Asynchronous Programming in Java: Options to Choose from
* https://devoxx.be/talk/?id=64003
* https://youtu.be/1zSF1259s6w?si=xcstf3NZWhn0SNfK

## Server Side Java
#### Spring Infrastructure Deep Dive: Virtual Threads, Checkpoint Restore, Native Images
* https://devoxx.be/talk/?id=20285
* https://www.youtube.com/watch?v=YfFYTR8_lBY
##### The impact of virtual threads
  * Two incarnations of thread (5:50):
    * Platform therad (PT) - traditional operating system thread
    * Virtual thread (VT)
  * VT is attacted to PT whenever it performs work
  * VT has abitilty to detach itelf from a PT whenever it hits a blocking point (so, it is never blocks a platfoem thread)
  * Whenever a blocking conditions is being released, a VT is reatached to PT again
  * The most important aspect of adopting VT in a Spting stack is the server container setup (8:57)
  * Traditional Spring MVC setup (on either Tomcat or Jetty) runs withing a thread pool managed by a server container:
    *  Server container has an HTTP connector;
    *  A connector has an executor attached
    *  Whenever a request comes in it dispatches a servlet thread to Spring MVC's dispatcher servlet and Spring takes it from there.

##### Deep dive: Spring's runtime efficiency theme

##### Deep dive: Spring's cleint-side HTTP support
