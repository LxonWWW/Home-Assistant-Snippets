# Home Assistant Spotify listening History
`"Home Assistant, whats this song?"`

![](https://raw.githubusercontent.com/LxonWWW/Home-Assistant-Snippets/main/spotify-listening-history/5.png)

### Step 1

Set-up your Spotify integration here: https://www.home-assistant.io/integrations/spotify/

### Step 2

Create a input_boolean at your helpers called "spotify_track_info". (http://homeassistant.local:8123/config/helpers)

![](https://raw.githubusercontent.com/LxonWWW/Home-Assistant-Snippets/main/spotify-listening-history/1.png)

### Step 3

Create a new (local) calendar named "spotify_song_list".

![](https://raw.githubusercontent.com/LxonWWW/Home-Assistant-Snippets/main/spotify-listening-history/2.png)

### Step 3

Replace all "spotify_YOUR_NAME" in "spotify_listening_history.yaml" and paste it into a new automation.

### Step 4

Create a new dasboard as a panel and subview and paste the following code there:

```
square: false
columns: 1
type: grid
cards:
  - initial_view: dayGridDay
    type: calendar
    entities:
      - calendar.spotify_song_list
    title: Hörverlauf
```

![](https://raw.githubusercontent.com/LxonWWW/Home-Assistant-Snippets/main/spotify-listening-history/3.png)
