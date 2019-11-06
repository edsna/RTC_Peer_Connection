Streaming a video with RTCPeerConnecton.


In short, RTCPeerConnection is an API used for making WebRTC calls to stream video, audio, and exchange data.

This web application uses RTCPeerConnection to set up a connection between two RTCPeerConnection objects (known as peers) on the same page. Ideally, this would happen with peers using different machines. However, for the purpose of demonstration of how RTCPeerConnection works, I'm establishing a connection between two objects on the same screen.

The entire process happens in three simple steps: We first create an RTCPeerConnection for each end of the call and, at each end, add the local stream from getUserMedia() API. When this is done, we get and share network information between the two ends/peers. This can also be called ICE candidates - basically a networking technique used to allow two computers to connect to each other as directly as possible. When this is done, we get and share metadata about local media in SDP format, - a format for describing streaming media parameters.

Please, remember that in order to run this sample code and have your camera accessible, you need to have it on your (local) web server. Clicking on the html link alone will only load the layout of the page. Why? because the browser will block the getUserMedia API if you don't serve it from a local web server. Even in the case of a web server, you need to 'allow' this permission when prompted because this option is desabled by default. If you don't have server space, I would strongly recommend using the Google Chrome's Web Server Extension, it is extremely easy to work with.  

Regards,
Edson Zandamela"# RTC_Peer_Connection" 
