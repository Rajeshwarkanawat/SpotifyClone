# Spotify Web Player Clone

A functional clone of the Spotify web player built using HTML, CSS, and JavaScript. The application allows users to explore albums, play songs, adjust volume, and navigate through playlists, emulating a simplified music streaming platform.

## Features

### 1. Dynamic Functionality
- **Music Playback**: Play, pause, and switch between songs using custom controls.
- **Volume Control**: Adjust the volume using a slider or toggle mute.
- **Progress Bar**: Seek through the song using a dynamic progress bar that updates in real time.
- **Song Metadata**: Display song information, including name and duration.
- **Playlist Navigation**: Automatically generate playlists by fetching song data dynamically from the server.

### 2. Unique Features
- **Album Display**: Dynamically fetch and display albums with metadata (title, description, and cover image) from the server.
- **Responsive Design**: Optimized for various devices, ensuring usability across different screen sizes.
- **Hamburger Menu**: Collapsible navigation menu for accessing the library and additional features.
- **Keyboard-Free Operation**: Entirely operable using mouse interactions for enhanced accessibility.

### 3. Responsive Design
- The layout adapts to both desktop and mobile screens.
- A hamburger menu provides seamless navigation on smaller screens.

## How Data Flows

### **1. Album Loading**
- Albums are fetched from the server's `/songs/` directory.
- For each album:
  - Metadata is retrieved from an `info.json` file.
  - Cards are dynamically created and appended to the album list.

### **2. Playlist and Song Management**
- When an album card is clicked:
  - The corresponding folder is accessed to fetch available songs.
  - Songs are listed with metadata (name and artist).
  - Clickable `Play Now` buttons allow immediate playback of a selected song.

### **3. Music Playback**
- Songs are streamed using the `<audio>` object.
- Playback controls include:
  - **Play/Pause**: Toggle between play and pause states.
  - **Previous/Next**: Navigate between songs in the playlist.
  - **Volume Slider**: Adjust the playback volume.
  - **Mute/Unmute**: Toggle sound on/off.

### **4. Real-Time Updates**
- The progress bar and current playback time are updated using the `timeupdate` event.
- User interactions with the seek bar update the playback position.
