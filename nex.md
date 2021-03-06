<!-- TITLE: NEX -->
<!-- SUBTITLE: Overview & documentation on Nintendo's semi-proprietary networking library. -->

# Overview
From **Kinnay**'s documentation (https://github.com/Kinnay/NintendoClients/wiki/):
> Nintendo offers a networking library called NEX.
>
> NEX provides functions to connect and talk to game servers. Nintendo hasn't written it from scratch. It's based on Quazal Rendez-Vous, so some things like the PRUDP Protocol may be seen in other games that use Quazal.

The NEX library is used for the majority of online-enabled titles. This brings about a problem though - as mentioned in **Kinnay**'s wiki:
> Unfortunately, there are many different versions of the nex library which are not backwards compatible, and even game-specific patches.

Its entirely possible that there are even update-specific patches for certain titles, but this has yet to be confirmed to **SuperMarioDaBom**.

**Stary2001** is developing a NEX dissector that can parse PRUDPv0/1 (for WiiU/3DS) for Wireshark (https://github.com/Stary2001/nex-dissector)

# Items of Interest
In this section, you will find interesting tidbits that you may find useful to know if you're making and/or utilizing NEX and its libraries and protocols.
**Notice:** Items contained here are observations made by the Pretendo team and various others. With that being said, its entirely possible that these observations are indeed false or at the very least not entirely true. So take what you see here with a grain of salt.
1. Within a single client-server instance, each end has their own RC4 stream.
2. PRUDP packets are considered "reliable" (aka they have the RELIABLE flag) only after the SYN and CONNECT handshakes have been completed (when the client starts sending DATA packets). If the handshake is incomplete, the packet should be considered unreliable.
3. When dealing with RMC, there are two ways to send errors. The first way is to send an RMC error. The other is to send an RMC success with the error code as the result code. Generally, **these two are not interchangeable**. If the error comes from the NEX protocol, then an RMC success payload should be used. This *probably* includes errors such as "invalid protocol id" or "invalid method id". If the error comes from trying to handle the RMC payload itself, then an RMC error should be used.
