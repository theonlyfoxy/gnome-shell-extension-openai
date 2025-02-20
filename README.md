# ChatGPT / OpenAI GNOME Extension

![desktop.gif](docs/desktop.gif)
![screenshot-overlay.png](docs%2Fscreenshot-overlay.png)

## ChatGPT Overlay for GNOME Shell

---

<div align="center">
This is a simple extension that uses the OpenAI API to display a ChatGPT Overlay by pressing


`Super + G`.

Note: API-Key is required for this extension.
If you look for an extension without API-Key you can
use [this one](https://github.com/HorrorPills/ChatGPT-Gnome-Desktop-Extension)
</div>

---

#### Features

- Supports Light/Dark Mode
- Settings UI
- Clear History (Shortcut: CTRL+L)
- Optional System Prompt (Initial prompt for all questions)

## Install From Source

This method installs to your `~/.local/share/gnome-shell/extensions` directory from the latest source code on the main
branch.

Clone this repository:

```bash
git clone https://github.com/theonlyfoxy/gnome-shell-extension-openai && cd gnome-shell-extension-openai
```

Install the extension:

```bash
make install
```

Restart desktop:

- On X11: `ALT+F2` then type `r`
- On Wayland: Log-out and Log-In again

Enable the extension:

```bash
gnome-extensions enable openai-gnome@etixsoftware.de
```

Open the settings dialog and paste your OpenAI-API-Key:

```bash
gnome-extensions prefs openai-gnome@etixsoftware.de
```

Show the overlay with the shortcut:

```
-> Super+G to show the overlay
```

## Settings

You can configure some settings in the UI:

| Name          | Example Value               | Description                                                                                                                                                                                                                           |
|---------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Open-Api-Key  | sk-a3e4ea904daa31150934fe   | Your Openapi-Key                                                                                                                                                                                                                      |
| System-Prompt | Act as a Stackoverflow post | The initial message which is added before each conversation. ([Read more about it here](https://platform.openai.com/docs/guides/chat/instructing-chat-models)).<br> It is sent in the background and will not be visible in your Chat |
| Debug-Mode    | false                       | Only for development use. If enabled, no API calls are made. Instead a placeholder message is shown as response.                                                                                                                      |

## Compatibility

The Extension was tested on:

- Ubuntu 22.04, X11, GNOME Shell 42.5
- Ubuntu 23.04, Wayland, GNOME Shell 43.2
- Fedora 38, Wayland, Gnome Shell 44

Feel free to contribute if you found bugs or improved something.

## TODO
[] Add HotWord for Wake Up

[] Voice Recognition for Interaction using Voice

[] Other Interaction Methods...

## FAQ

#### Where can I get an OpenAI API-Key?

First you need to create an Account on [OpenAI](https://openai.com/blog/openai-api).

From your user profile, you can manage your API keys by selecting "Manage API Keys".

## Troubleshooting

- Restart GNOME Shell (`ALT+F2`, then type `r`)
- Look for error messages in

```
journalctl /usr/bin/gnome-shell
```

## License

This Extension has been released under The GNU General Public License v3.0.
