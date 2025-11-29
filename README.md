# Metro Slate Light for Home Assistant

A modernized Home Assistant theme based on the Metro design language, featuring a slate blue-gray color scheme with crisp typography and clean aesthetics.

This is a modernized, single-theme version extracted from the [Metrology for Home Assistant](https://github.com/Madelena/Metrology-for-Hass) theme collection by Madelena Mak. Updated to Home Assistant 2025.5+ standards with deprecated variables removed and new typography system variables added.

## About This Theme

**Metro Slate Light** brings Microsoft's Metro design language to Home Assistant with:

- **Slate blue-gray color palette** (#4f5a68 primary, #677385 accent)
- **Sharp, zero-radius corners** characteristic of Metro design
- **True white backgrounds** (rgb(255,255,255)) for clarity
- **Segoe UI typography** for authentic Windows aesthetic
- **No box shadows** maintaining the flat Metro style
- **Updated for HA 2025.5+** with modern CSS variables

## Features

- Display your home automation status with distinct and bold typography using Segoe UI fonts
- Metro design language with sharp corners and vibrant color contrast
- True white background optimized for clarity and readability
- Extensive card-mod customizations for system-wide UI enhancements
- Revamped More Info cards and dialogs with blur effects
- Compatible with Mushroom cards and other popular custom cards
- Updated to current Home Assistant theme variable standards

## How to Install the Theme

### Prerequisites

- Home Assistant installation
- Some way to upload files to your HA server (e.g., Visual Studio Code, Samba, or File Editor add-ons)
- [card-mod](https://github.com/thomasloven/lovelace-card-mod) (required for full styling)

### Installation

1. If you are new to Home Assistant themes, first add this to your `configuration.yaml` file:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes
   ```

2. Create a new folder named `themes` under your `/config` directory if it doesn't exist.

3. Copy [`metro.yaml`](/themes/metro.yaml) to `/config/themes/`.

4. (Optional but recommended) To use Segoe UI fonts on non-Windows devices:
   - Copy [`style.css`](/www/style.css) and all `.ttf` font files from the `/www` folder to `/config/www/`.
   - Add the stylesheet to your Lovelace resources:
     - **If using UI mode**: Go to Settings → Dashboards → Resources, then add `/local/style.css` as a Stylesheet.
     - **If using YAML mode**: Add to your Lovelace configuration:
       ```yaml
       lovelace:
         mode: yaml
         resources:
           - url: /local/style.css
             type: css
       ```

5. Restart Home Assistant to apply the changes.

6. Once restarted, go to your Profile page (click your avatar at the bottom left).

7. Under **Themes**, select **"Metro Slate"**.

8. Under **Theme Mode**, select **"Light"** (this is a light-mode only theme).

### Font Notes

- Segoe UI font is already installed on Windows devices
- For non-Windows devices, you can download official Segoe UI Variable fonts from [Microsoft's Design Downloads](https://docs.microsoft.com/en-us/windows/apps/design/downloads/#fonts)
- The theme will fall back to system fonts if Segoe UI is not available

## What's Been Updated

This modernized version includes:

### Removed (Deprecated as of HA 2025.5)
- All `paper-*` prefixed variables (paper-slider, paper-toggle-button, paper-font, etc.)
- Legacy `light-theme-*` and `dark-theme-*` variables
- Outdated card/dialog variables

### Added (HA 2025.5+ Standard)
- `ha-font-family-body`
- `ha-font-size-*` variables (2xs through 4xl)
- `ha-font-weight-*` variables (light through bold)
- `ha-card-header-font-weight`
- Modern slider and card variables

### Fixed
- Syntax error in sidebar-selected-text-color variable
- Replaced deprecated paper-slider with modern slider variables
- Updated dialog/card variables to current naming conventions

## Credits

This theme is based on [Metrology for Home Assistant](https://github.com/Madelena/Metrology-for-Hass) by Madelena Mak.

Original theme design language based on [Metro](https://en.wikipedia.org/wiki/Metro_(design_language)) and [Fluent](https://www.microsoft.com/design/fluent/) design systems pioneered by Microsoft Design.

The initial Metrology code was partially based on [JuanMTech's AMOLED Theme](https://community.home-assistant.io/t/amoled-blue-theme-juanmtech/164458).

![Creative Commons License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png)

This work is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/).

Original design by [Madelena Mak](https://MadelenaMak.com). Modernization and single-theme extraction for personal use.
