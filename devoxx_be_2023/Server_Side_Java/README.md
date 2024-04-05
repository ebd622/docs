# Server side Java
### Spring Infrastructure Deep Dive: Virtual Threads, Checkpoint Restore, Native Images
* https://devoxx.be/talk/?id=20285
* https://www.youtube.com/watch?v=YfFYTR8_lBY
#### The impact of virtual threads
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

#### Deep dive: Spring's runtime efficiency theme

#### Deep dive: Spring's cleint-side HTTP support (1:20:10)
* RestTemplate intorduction 15 years ago: Upsides and Downsides (1:22:15)
* WebClient introduced in Spring5 (1:27:00)
* VT (1:29:15)
  * Spring Framework 6.1 sipports VT
  * Spring Boot 3.2 offers a property `spring.threads.virtual.enabled`. Setting it to `true` will enable VT for Tomcat&Jetty. (cleint applications will be running on VTs)
* Use WebClient instead of RestTemplate? (1:34:00)
* RestClient: The API of WebClient with the (improved) infrastructure of RestTemplate (1:35:00)
* Demo and samples (https://github.com/poutsma/restclient-sample) (1:35:36)
  * Use Parameeterized Types (1:49:11)
  * Error Handling (1:53:48)
  * Exchange method (1:57:40)
  * ClientRequestFactories (2:01:22)

## Prepare for Jakarta EE 11!
* https://devoxx.be/talk/?id=6261
* https://www.youtube.com/watch?v=8ke0kPrg9qc
* https://www.agilejava.eu/2023/09/05/jakarta-ee-11-is-shaping-up/
