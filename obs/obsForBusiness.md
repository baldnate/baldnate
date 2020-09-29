# Crash Course in OBS

Note: This document is focused on using OBS with a slant towards _business usage_.

## Why?

The three reasons OBS might be useful to you are:
- Streaming video content that MS Teams, et al don't handle well
- Recording video content for publication or for further editing
- Setting up a virtual webcam

## Getting started

Go get OBS from [their website](https://obsproject.com/), install it on your machine, and run it.  Then go through [this tutorial](https://www.youtube.com/watch?v=wAvQfjpZncY) or one of the many other OBS tutorials on YouTube.  The important things to learn are basic navigation in OBS and the core concepts of scenes and sources.  I recommend setting up a couple of scenes for the following likely business situations as an exercise:
- Powerpoint or Excel with your webcam to the side or on top.  Experiement with adding a filter on your webcam to make it partially transparent if you wish to superimpose your camera over your business application.
- Capture your web browser and verify that it works as expected.  You may need to use a "Game Capture" source instead of a "Window Capture" source.  This trick can apply to other applications as well: it is just a different mode of capture designed for games primarily, but is sometimes needed for non-game applications as well.
- Create a "Be Right Back" scene that you can switch to during a live presentation.

At this point, you should have enough knowledge to record yourself presenting a slide deck with commentary.  Congrats!  Now you know how to create simple recordings of yourself with or without additional content, as well as the basics of scene construction in OBS.

## Streaming

Streaming from OBS isn't technically difficult, but smoothly producing a stream that looks and sounds professional requires more technical preparation.  Here are topics you should spend more time looking into to smooth out rough edges:

- Transitions: Crossfades are a simple way to make your scene swaps less jarring.  Just configure it in OBS and forget it.
- Audio Management: Virtual audio cables and a virtual mixer will make it much easier to wrangle all your audio during a stream.  In particular, if you are restreaming content from others during a live event, being able to isolate your streamed audio sources from the rest of your system sounds is essential.  There are many videos on this topic on YouTube.
- Audio Mixing: The other challenge you'll have is getting all your audio levels just right.  This applies even if the only audio in your stream/recording will be your voice.  Research your type of microphone to understand how your should be positioning it relative to your mouth and to ambient noise sources.  If you have GPU to spare, consider using RTX Voice to help filter out non-voice noise.  If you find that your voice volume fluctuates distractingly during a session, consider adding a compressor filter to your mic source in OBS.  There is a whole world of hardware and software tools for audio management, but it takes time to learn them and apply them in a way that improves your audio quality.  My recommendation is to start without filters and just adjust your microphone position and gain first, then add RTX Voice (or a different brand of AI based noise supression) and/or compressors to the mix.
- Understanding the streaming platforms: OBS supports several services as well as custom streaming servers.  Unless your company has already provided guidance on what streaming services are appropriate for what kinds of corporate material, you'll need to do some research.  I talk about about the major players later in an appendix.

The good news for most of these items is that you can try them out in local recordings first.  You can also set up unlisted YouTube streams to get your co-workers to help you out with testing.

### Virtual Webcam

A virtual webcam allows you to customize the video going into your video chat software.  If that sounds appealing, then there are many online tutorials for how to go about this using OBS and free plugins.  In short, you can use a virtual webcam to allow you to use all of what you have learned above to customize what your webcam looks like in other applications.  I personally don't use a virtual webcam, but if you spend much of your professional time in Teams/Zoom/Skype video meetings, this could be useful.

### Wrap Up

I purposely don't go deep here because I did not wish to duplicate or retread what has already been created by so many other folks already.  However, if there is a particular topic you would like more framing or detail on, let me know and I will consider it.

## Appendicies

### Streaming Services

#### Twitch

Twitch is a channel-centric streaming service focused primarily on gaming, but has significant non-gaming content as well.  The channel-centric concept means that the primary mode of navigation and discovery is via _channels_.  A channel is either live or offline.  Twitch does support recorded content through past broadcasts, highlights,and clips.

The primary drawback with using Twitch for business purposes is access control.  There are only two options for stream viewing restrictions: fully public, or subscriber only.  In Twitch terms, a subscriber is a person who has paid money for premium access to your channel.  Neither of these options matches well with using Twitch to host a stream that only co-workers are meant to watch.  Also, Twitch runs ads over your stream.  At the moment, the typical ad experience is a pre-roll ad: when first connecting to your stream, the viewer will be forced to watch a short commerical.  Note that many ads on Twitch would not be considered corporate friendly.

In short: unless your business wishes to stream out to the world, Twitch is unlikly to be a good match for corporate streaming.

#### YouTube

YouTube is a video-on-deman (VOD) centric service that has no single dominant content-subject specialization.  Live streaming was added long after the platform launched, and in some regards it makes for a clunkier streaming experience.

However, YT streaming does offer more options for access control.  There are three levels: private, unlisted, and public.  Unlisted is an attractive option for limited access corporate streaming: your stream will not appear thorough YT search, but anyone with the link to your stream can tune in.  This is an improvement over Twitch options, but it isn't what most IT departments would want for truly sensitive material.

#### Custom Streaming to an RTMP Server

The most configurable option is to run your own RTMP server and stream to it.  It is the most involved, but also affords you the most control.  There are free and open options for this, and OBS supports this out of the box.  The viewer experience will also be different: they will either need to use stream viewing software like VLC or mpv, or you will need to set up a web front end for the stream.  There may be canned solutions for the last option, but I have not researched it yet.
