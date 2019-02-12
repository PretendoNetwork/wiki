<!-- TITLE: NEX -->
<!-- SUBTITLE: Overview & documentation on Nintendo's semi-proprietary networking library. -->

# Overview
From **Kinnay**'s documentation (https://github.com/Kinnay/NintendoClients/wiki/):
> Nintendo offers a networking library called NEX.
>
> NEX provides functions to connect and talk to game servers. Nintendo hasn't written it from scratch. It's based on Quazal Rendez-Vous, so some things like the PRUDP Protocol may be seen in other games that use Quazal.

# Items of Interest
In this section, you will find interesting tidbits that you may find useful to know if you're making and/or utilizing NEX and its libraries and protocols.
**Notice:** Items contained here are observations made by the Pretendo team and various others. With that being said, its entirely possible that these observations are indeed false or at the very least not entirely true. So take what you see here with a grain of salt.
* Each PRUDP packet requires its own RC4 stream. If the stream isn't reset between packets, the encryption gets encrypted weird and the console is unable to read the packet. While **SuperMarioDaBom** hasn't observed this with every RC4 library, he has seen it with the implementation that nex-go uses.