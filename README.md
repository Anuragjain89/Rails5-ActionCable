# ACTION CABLE

One of the best thing about rails is the ease with which it allows you to ** develop webapps quickly by providing some sensible defaults. **

And with Rails 5, it allows you to make real time web apps in a breeze

> Introducing Action Cable.. a real time framework for communication over websockets.

But before we proceed any further, let's spend some time discussing how we got to the action cable.. or particularly, the web sockets.

When web started becoming more dynamic with ajax and js advances, we, as developers, started finding ways to make our applications more real-time.

## POLLING

One of the earliest solution that we came up with was Polling.

> Client sends request at regular intervals.
>
 What a simple and robust solution to implement !!

The interval plays a critical role here:

In order to give any real-time experience to the client, ***the polling interval needs to be small*** enough to make the user effectively believe that app is almost live with some network latency may be.

> But there were problems :
>
If we try to make it more realtime by reducing polling interval, our servers didn't like it mainly because of the way the polling.. or rather HTTP works.


HTTP is a **stateless** protocol. The server and client are aware of each other only during the current request. Afterwards, both of them forget about each other.

Which means... ?

For each request, there is additional data in the form of headers which gets transmitted through the network and therefore, the communication was inefficient.
