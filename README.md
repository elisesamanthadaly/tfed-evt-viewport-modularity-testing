# tfed-evt-viewport-modularity-testing

https://elisesamanthadaly.github.io/tfed-evt-viewport-modularity-testing/

- This is a very poorly built demo to drag/drop and delete instances of multiple EVTs using iframes

- To get a local instance of EVT to run on Chrome, I had to create a Chrome shortcut and add "-allow-file-access-from-files" as a launch parameter.

- We appear to be missing an images folder (needed for both the manuscript image displays and the various buttons on the app). I borrowed the images and fonts folders from the current EVT build: https://github.com/evt-project/evt-viewer, but that hasn't fixed all the buttons (need to check files + relative pathing)

- Likewise, it seems like the original folder structure of the Aelfric EVT app wasn't preserved in either Hunter or Jacob's repositories. E.g., when index.html is looking for "scripts/whatever.js," but we don't have a scripts folder. So far I've only had to change 5 relative path links to make things work for testing functionality-- two css links in index.html (lines 13 and 15), two script links in index.html (lines 352 and 353), and line 6 ("dataUrl") in config.json.

- Line 32 of Bolougne.xml, fixed mismatched end tag so xml is readable
