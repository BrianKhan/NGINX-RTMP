## NGINX-RTMP ##
A manual for creating and maintaining a server capable of handling disconnections during RTMP data streams

## What is RTMP ###
RTMP, Real Time Media Playback, the core building block of video streaming pipelines used in applications like Twitch or YouTube live streams. RTMP is a rich protocol, released in 2012 by Adobe with a [mature and lengthy specification](http://wwwimages.adobe.com/www.adobe.com/content/dam/acom/en/devnet/rtmp/pdf/rtmp_specification_1.0.pdf) ; the spec allows for both video reception and playback to clients accross networks. However, the specification has not been updated since it's release.



Typically, the pipeline works as follows:
A device submits a video stream to a server via the RTMP protocol. The URL usually looks something like rtmp://StreamSite.com/app/name
A larger scale deployment will have different [ingest servers](https://stream.twitch.tv/ingests/) in multiple areas ready to accept the connection

