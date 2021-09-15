# ChatEx

A chat extension mod for StarCraft 2

[![ChatEx Demo Thumbnail](https://user-images.githubusercontent.com/19297229/133377628-775ad9f8-165e-4e96-90a9-1191dcbdb3d5.png)](https://www.youtube.com/watch?v=dYxYuVyVPV0)


## Features

ChatEx builds on top of the default chat and adds the following:

- Live typing indicator: displays a list of players that are currently typing
- Dynamic chat display: the chat display can be moved and resized
- Persistent chat: the chat display can be pinned which prevents messages from fading away over time
  - Hovering over the chat display will unfade old messages and darken the background to increase readability
- The chat bar is now multiline and will expand or shrink it's height based on the chat bar's contents
- Recent message history: players can retrieve past chat messages that they've sent
- Optional features that can be easily disabled based on your project's use case
  - A button to hide the chat display and live typing indicator
  - Cinematic Mode: players can toggle showing/hiding the game UI 
  - RPG Camera: when enabled makes the currently selected unit and moving the mouse while holding down the mouse wheel will orbit the camera around the unit
  - Chat Bubbles: when enabled chat messages will be displayed in a chat bubble above the currently selected unit and text in parentheses will be italicized in the chat bubble

## Installation

ChatEx is published as a public extension mod named `ChatEx Chat Extension` on Blizzard's SC2 services. To add ChatEx to your map do the following:

1. Open your .SC2Map or .SC2Mod file in the SC2 editor
2. On the menu bar near the top left of the editor window click on `File>Dependencies...`
3. Below the left pane of the window that pops up click on `Add Other...`
4. On the next window click on the `Blizzard` tab near the top left corner
5. Log in to your Blizzard account
6. Set the `Source:` dropdown to `Map/Mod Name`
7. In the textbox to the right of the dropdown type `ChatEx` then click the `Go` button to the right of the textbox
8. Check the `Always Use Latest Version` checkbox
9. Select `ChatEx Chat Extension` in the list and then click on `Ok`

## Configuring ChatEx

1. Open your .SC2Map or .SC2Mod file in the SC2 editor
2. Open the editor's UI Module by clicking on `Modules>UI (Shift+F6)` in the menu bar near the top left of the editor
3. Add a layout file named `ChatEx_Config` by right clicking on the file tree pane on the left of the UI Module window and selecting `Add Layout (Ctrl+L)`
4. Replace the `ChatEx_Config` file's contents with the code snippet below

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes"?>
<Desc>
    <Constant name="ChatEx_RpgCameraButton_Visible" val="true"/>
    <Constant name="ChatEx_ChatBubblesButton_RightOffset" val="0"/> <!-- Button width = 32 -->
    <Constant name="ChatEx_CinematicModeButton_Visible" val="true"/>
    <Constant name="ChatEx_ChatBubblesButton_Visible" val="true"/>
    <Constant name="ChatEx_ChatBubblesButton_LeftOffset" val="0"/> <!-- Negative value moves the button to the left -->
    <Constant name="ChatEx_HideChatDisplayButton_Visible" val="true"/>
</Desc>
```

5. Modify the `val` attributes as needed
6. For more advanced customization options consider:
  - Using triggers, UI/Layout modding or the Text Module
  - Creating a seperate dependency mod that overrides ChatEx's SC2Layout files

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## History

- 2021-09-13 - Project made publicly available

## Credits

Just [@Cabcase](https://github.com/Cabcase) for now, but hopefully more people soon! 

## License

Whatever Blizzard's [EULA](https://www.blizzard.com/en-us/legal/fba4d00f-c7e4-4883-b8b9-1b4500a402ea/blizzard-end-user-license-agreement) and [Custom Game Policy](https://www.blizzard.com/en-us/legal/2749df07-2b53-4990-b75e-a7cb3610318b/custom-game-acceptable-use-policy) mandate.

MIT License for everything else.

Copyright (c) 2021 Cabcase

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
