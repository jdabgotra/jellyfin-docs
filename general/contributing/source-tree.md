---
uid: contrib-source-tree
title: Source Tree
---

# Source Tree

Jellyfin is a maze of clients, plugins, and other useful projects. These source trees can serve as an excellent tool to inform new developers about the structure of several projects.

## [Jellyfin Server](https://github.com/jellyfin/jellyfin)

01. BDInfo: `Blu-Ray Analyzer`
    - Properties: `Assembly Info`
02. DvdLib: `DVD Anaylzer`
    - Ifo:
    - Properties:
03. Emby.Dlna:
    - Profiles: `DLNA Profiles for clients`
04. Emby.Drawing:
05. Emby.Naming:
06. Emby.Notifications:
07. Emby.Photos:
08. Emby.Server.Implementations:
    - ScheduledTasks: `all scheduled tasks can be found here`
09. Jellyfin.Api:
10. Jellyfin.Drawing.Skia:
11. Jellyfin.Server:
12. MediaBrowser.Api:
    - Playback:
      - BaseStreamingService.cs: `receives client information and reads media info and feeds this info to MediaInfoService`
      - MediaInfoService.cs: `logic for the stream builder that determines method of playback such as Direct Play or Transcoding`
13. MediaBrowser.Common:
14. MediaBrowser.Controller:
15. MediaBrowser.LocalMetadata:
16. MediaBrowser.MediaEncoding:
17. MediaBrowser.Model:
18. MediaBrowser.Providers:
19. MediaBrowser.WebDashboard:
20. MediaBrowser.XbmcMetadata:
21. RSSDP:
22. benches/Jellyfin.Common.Benches:

## [Web Client](https://github.com/jellyfin/jellyfin-web)

1. src:
    - assets: `images, styles, splash screens, and any other static assets`
        - css: `all global stylesheets used throughout the client`
        - img: `images for things like device icons and logos`
        - splash: `progressive web apps will show these splash screens`
    - components: `custom elements used for different sections of the user interface`
        - playerstats.js: `display playback info in browsers and other clients that include the web source`
    - controllers: `scripts that handle the logic for different pages`
    - elements: `custom UI components that are used globally such as buttons or menus`
    - legacy: `currently used for all polyfills and scripts related to backwards compatibility`
    - libraries: `dependencies that we eventually want to remove and include during the build step`
    - scripts: `any script that isn't tied to a UI element or page but rather general functionality`
    - strings: `translations for the entire interface`
    - themes: `custom and bundled themes can be found here in their own directories`

## [Android](https://github.com/jellyfin/jellyfin-android)

1. res:
   - android:
2. src:
   - NativeShell:
     - res:
     - src:
       - RemotePlayerService.java: `handles the notification tile that can control playback`
     - www:
   - cordova:

## [Android TV](https://github.com/jellyfin/jellyfin-androidtv)

1. app:
   - src:
     - main:
       - java/org/jellyfin/androidtv:
         - constant: `constants/enums`
         - data:
           - compat: `classes ported from old apiclient to maintain compatibility in the app (Deprecated should be replaced/removed)`
           - eventhandling: `API webservice event handling`
           - model: `various data models`
           - querying: `extensions to the querying package in the apiclient (Should probably be replaced/removed)`
           - repository: `data repositories for shared access`
         - di: `dependency injection modules`
         - integration: `Android TV homescreen channel integrations`
         - preference: `interface for Android shared preferences`
         - ui:
           - browsing: `views for browsing items (rows, grids, etc.)`
           - home: `home screen views`
           - itemdetail: `item detail views`
           - itemhandling: `BaseItem views`
           - livetv: `live TV views`
           - playback: `media player views`
           - preference: `app preferences/settings views`
           - presentation: `presenters from MVP architecture`
           - search: `search views`
           - shared: `shared code for UI classes`
           - startup: `authentication views`
         - util: `various utilities`
       - res: `Android resource files for XML layouts, translations, images, etc.`

## [Kodi](https://github.com/jellyfin/jellyfin-kodi)

1. jellyfin_kodi
   - database: `manipulating the local Jellyfin sqlite database`
   - dialogs: `code behind popup menus for user interaction`
   - entrypoint: `main addon settings page`
   - helper: `small helper functions, mostly formatting or reused functions`
   - jellyfin: `interacting with the server`
   - objects:
     - kodi: `handling local Kodi media types and database`
2. resources:
   - language: `string files for localization`
   - skins: `design of popup menus for user interaction`
