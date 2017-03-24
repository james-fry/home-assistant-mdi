# Index of MDI Icons that are suitable for Home Assistant

This project is based on the preview.html from the MDI webfont hosted here https://materialdesignicons.com/getting-started
I have kept all the files from the original webfont and added the following:

- home-assistant-mdi.html: renders the index
- HA_MDI_JSON.xlsx: my tool to create the JSON used by JS in home-assistant-mdi.html
- Updated the readme

## Installation

- Clone the repo into the HA local www folder that should be located in the same directory as your HA config files
- Update your HA configuration.yaml file to add an iframe pointing to local file home-assistant-mdi:
'''
panel_iframe:
  mdiindex:
    title: MDI Icon Index
    icon: mdi:vector-square
    url: http://localhost:8123/local/home-assistant-mdi.html
'''
- Restart Home Assistant to pick up the new panel_iframe, which will add a MDI icon on the panel

## Usage

- Click on the MDI icon to open the index
- Browse to find an appropriate icon
- Click icon or name to copy the icon name (with mdi: prefix) ready to paste into config yaml etc
