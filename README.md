# Index of MDI Icons that are suitable for Home Assistant

This project is based on the preview.html from the MDI webfont hosted here https://materialdesignicons.com/getting-started
I have kept all the files from the original webfont and added the following:

- home-assistant-mdi.html: renders the index
- HA_MDI_JSON.xlsx: my tool to create the JSON used by JS in home-assistant-mdi.html
- Updated the readme

## Installation
The following was tested with HA running in Docker on Ubuntu.
I am currently running with no SSL/TLS, so not tested with HTTPS.

### Easy Method - use raw.githack.com (now that rawgit is closing down): 
- Edit your HA configuration.yaml file to add an iframe using rawgit direct URL to my repo:
```yaml
panel_iframe:
  mdiindex:
    title: MDI Icon Index
    icon: mdi:vector-square
    url: https://raw.githack.com/james-fry/home-assistant-mdi/master/home-assistant-mdi.html
```
- Restart Home Assistant to pick up the new panel_iframe, which will add a MDI icon on the panel

### Harder Method - clone my GH repo locally
- cd to HL local www folder - typically this is located (or needs to be created) in the same directory as your HA config files
- Clone the repo into the HA local www folder: *git clone https://github.com/james-fry/home-assistant-mdi*
- Edit your HA configuration.yaml file to add an iframe pointing to local file home-assistant-mdi html:
```yaml
panel_iframe:
  mdiindex:
    title: MDI Icon Index
    icon: mdi:vector-square
    url: http://localhost:8123/local/home-assistant-mdi/home-assistant-mdi.html
```
- Restart Home Assistant to pick up the new panel_iframe, which will add a MDI icon on the panel

You should see this:

![Missing image showing Home Assistant with the MDI Icon Index](https://github.com/james-fry/home-assistant-mdi/raw/master/images/ha_mdi.png "Home Assistant with the MDI Icon Index")

## Usage

- Click on the MDI icon on HA panel to open the index
- Browse to find an appropriate icon for your sensor/device/room etc
- Click the icon or mdi:name to copy the icon name (with mdi: prefix) ready to paste into config yaml etc

## To Do

- Fully list weather icons
- Fully list battery icons
- Fix non-printing icos (if possible)
