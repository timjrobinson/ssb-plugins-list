# ssb-plugins

A list of all [Secure Scuttlebutt](https://scuttlebutt.nz) plugins and high level overview of what they do. For other Scuttlebutt apps/docs/tutorials that aren't plugins check out [awesome-ssb](https://github.com/mttmyr/awesome-ssb).

- [ssb-server](https://github.com/ssbc/ssb-server) - The core Scuttlebutt server, previously called scuttlebot. Not a plugin itself, it loads all the Scuttlebutt plugins and exposes their API's on the sbot objects that it returns after initialization.
- [ssb-keys](https://github.com/ssbc/ssb-keys) - Deals with creating your keys, signing log messages with your keys, and verifying signed messages ensuring they are legitimately written by the owner of that log.
- [ssb-links](https://github.com/ssbc/ssb-links) - Handles all the links between SSB posts. For example when someone replies to a post they create a post on their personal feed with a link to the post they are replying to. ssb-links creates the database indexes so that when anyone goes to view a thread the application can quickly find all replies without having to scan every post in the database.
