## NGINX-RTMP ##
A manual for creating and maintaining a server capable of handling disconnections during RTMP data streams

### RTMP and history ###
RTMP, Real Time Media Playback, the core building block of video streaming pipelines used in applications like Twitch or YouTube live streams. RTMP is a rich protocol, released publically in 2012 by Adobe with a [mature and lengthy specification](http://wwwimages.adobe.com/www.adobe.com/content/dam/acom/en/devnet/rtmp/pdf/rtmp_specification_1.0.pdf). The spec allows for both video reception and playback to clients accross networks. However, the specification has not been updated since it's public release.

Before it's public release in 2012, RTMP was a proprietary protocol developed by Macromedia. Being proprietary put Adobe in a unique position to create the best server-side software to accept and play back RTMP livestreams, called Flash Media Server. This caused a boom of live-streaming sites to pop up, the most notable of which being Justin.TV, evolving into Twitch.tv later on. Most of these sites ran on Flash Media Server before 2012, meaning they had little access to the backend of the video streaming pipeline, and customers had to view videos using Flash. Justin.TV and early Twitch.tv served their content through Flash, [only recently completely ditching the technology](https://old.reddit.com/r/Twitch/comments/70ah1m/has_twitch_removed_flash_player/). However, RTMP is still used as the protocol to ingest and stream video because it is mature, and scalable for ingest. To further understand why RMTP isn't great for direct-to-customer playback, we must understand the RTMP pipeline.



### The RTMP Pipeline: ###
A device submits a video stream to a server via the RTMP protocol. The URL usually looks something like rtmp://StreamSite.com/app/name
A larger scale deployment will have different [ingest servers](https://stream.twitch.tv/ingests/) in multiple areas ready to accept the connection

