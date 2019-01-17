<!-- TITLE: About -->
<!-- SUBTITLE: Info about the project and its history. -->

# What is Pretendo Network?
Pretendo Network is a WIP replacement for all Nintendo Network services for the Nintendo 3DS family of systems and the Wii U. These include multiplayer, accounts, eShop, Miiverse, and more! This project will help preserve those aspects of the consoles in the event that the official services get taken down.

# History
As told by the project's creator, RedDucks, himself:
> The whole project started shortly after Cemu (the Wii U emulator) got online capabilities.
> 
> Before online, a service called SMMDB was made to store and serve Super Mario Maker courses for Cemu users (you would download the courses you want and then inject them into your save, and upload courses you've made using their client/website).
> 
> I wanted to originally just make a bridge between SMMDB and Cemu using it's new online features. This led me to start researching SMM and it's REST api, along with several others (most of whom are part of Pretendo now).
> 
> It became clear soon after that we couldn't just patch the game to get courses from somewhere else, so we turned to making a custom SMM server (we also housed our docs on SMM on the same repo. This was before we knew about PRUDP (you can actually still see the original repo here https://github.com/RedDuckss/csms/ ))
> 
> Soon after that we realized the scope of the project and how large it was just for a custom bridge between SMMDB and Cemu. So then I started a more generalized service replacement project (again, before we knew about PRUDP) under the name RiiU.
> 
> I eventually found out about PRUDP, renamed the project Pretendo, met @SuperMarioDaBom and we began the first real attempt at a complete WiiU service replacement.
> 
> We only added 3DS games to the roadmap because they also utilize PRUDP, and people asked for it. Switch research is underway but we will not be releasing anything Switch related until after the official servers go down.