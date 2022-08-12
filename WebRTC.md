# What is WebRTC?

> WebRTC is a set of JavaScript API's that allow us to establish peer to peer connection between two browsers to exchange data such as audio and video in real time.

> Real time communication between browsers. 
> Data never touches server
> Real Time Communication
> Lower Latency
> WebRTC transports its data over UDP, UDP is fast.

### WebSockers

> Real time communication through server
> Not for audio and video

## So if WebRTC is so fast, why use WebSockets at all?

> UDP is not a reliable protocol for transferring important data
> No built in signaling
> UDP does not validate the data.

# WebSockets + WebRTC = 👍

## So what exactly is sent between the two clients and how is it sent?

> ### SDP's: A session Description Protocol (SDP), is an object containing information about the session connection such as the codec. address. media type, audio and video and so on.

> ### ICE Candidates: An Ice