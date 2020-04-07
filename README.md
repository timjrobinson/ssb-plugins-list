# SSB Plugins List

A list of all [Secure Scuttlebutt](https://scuttlebutt.nz) plugins and high level overview of what they do. For other Scuttlebutt apps/docs/tutorials that aren't plugins check out [awesome-ssb](https://github.com/mttmyr/awesome-ssb). You can find an up-to-date list of all plugins loaded by default in the [ssb-server bin.js file](https://github.com/ssbc/ssb-server/blob/master/bin.js#L45).

If you feel a plugin isn't sufficiently explained or doesn't make sense, please open an issue on this repository.

## Core Packages

- [ssb-server](https://github.com/ssbc/ssb-server) - The core Scuttlebutt server, previously called scuttlebot. Not a plugin itself, it loads all the Scuttlebutt plugins and exposes their API's on the sbot objects that it returns after initialization.
- [ssb-config](https://github.com/ssbc/ssb-config) - The default configuration for SSB Server. Not an SSB plugin. It returns a JSON configuration object with sane default settings. You can then pass it to the server when initializing it.  

## Core Plugins

- [ssb-blobs](https://github.com/ssbc/ssb-blobs) - Handles sending and receiving 'blobs' on the Scuttlebutt network. Blobs are larger binary format items such as images or video that are too large to add as a message to someones feed.
- [ssb-keys](https://github.com/ssbc/ssb-keys) - Deals with creating your keys, signing log messages with your keys, and verifying signed messages ensuring they are legitimately written by the owner of that log.
- [ssb-links](https://github.com/ssbc/ssb-links) - Handles all the links between SSB posts. For example when someone replies to a post they create a post on their personal feed with a link to the post they are replying to. ssb-links creates the database indexes so that when anyone goes to view a thread the application can quickly find all replies without having to scan every post in the database.
