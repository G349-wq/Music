# Music
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Music Player</title>
    <link rel="stylesheet" href="styles.css">
</head>

<body>
    <div class="container">
        <h1>Music Player</h1>
        <div class="music-player">
            <!-- Left Section (All Songs and Genre Filter) -->
            <div id="allSongsSection">
                <label for="genreFilter">Filter by Genre:</label>
                <select id="genreFilter">
                    <option value="All">All</option>
                    <option value="Pop">Pop</option>
                    <option value="Rock">Rock</option>
                    <option value="Jazz">Jazz</option>
                </select>

   <h2>All Songs</h2>
                <div id="allSongs">
                    <div class="song-item" data-genre="Pop" onclick="playSong('Shape Of You', 'Ed Sheeran', 'https://example.com/shape_of_you.jpg', 'https://example.com/shape_of_you.mp3')">
                        <button>Shape Of You - Ed Sheeran</button>
                    </div>
                    <div class="song-item" data-genre="Pop" onclick="playSong('All Of Me', 'Adele', 'https://example.com/all_of_me.jpg', 'https://example.com/all_of_me.mp3')">
                        <button>All Of Me - Adele</button>
                    </div>
                    <div class="song-item" data-genre="Rock" onclick="playSong('Wonderwall', 'Oasis', 'https://example.com/wonderwall.jpg', 'https://example.com/wonderwall.mp3')">
                        <button>Wonderwall - Oasis</button>
                    </div>
                    <div class="song-item" data-genre="Pop" onclick="playSong('Sugar', 'Maroon', 'https://example.com/sugar.jpg', 'https://example.com/sugar.mp3')">
                        <button>Sugar - Maroon</button>
                    </div>
                    <div class="song-item" data-genre="Pop" onclick="playSong('Locked Away', 'R. City', 'https://example.com/locked_away.jpg', 'https://example.com/locked_away.mp3')">
                        <button>Locked Away - R. City</button>
                    </div>
                    <div class="song-item" data-genre="Jazz" onclick="playSong('Feeling Good', 'Nina Simone', 'https://example.com/feeling_good.jpg', 'https://example.com/feeling_good.mp3')">
                        <button>Feeling Good - Nina Simone</button>
                    </div>
                    <div class="song-item" data-genre="Rock" onclick="playSong('Bohemian Rhapsody', 'Queen', 'https://example.com/bohemian_rhapsody.jpg', 'https://example.com/bohemian_rhapsody.mp3')">
                        <button>Bohemian Rhapsody - Queen</button>
                    </div>
                </div>
            </div>

     <!-- Center Section (Song Card) -->
   <div id="songCardSection">
                <div class="song-card">
                    <img src="https://example.com/shape_of_you.jpg" alt="Song Image" id="songImage" style="display: none;">
                    <h3 id="songTitle">Shape Of You</h3>
                    <p id="songArtist">Ed Sheeran</p>
                    <audio controls id="audioPlayer">
                        <source src="https://example.com/shape_of_you.mp3" type="audio/mpeg">
                        Your browser does not support the audio tag.
                    </audio>
                    <div class="controls">
                        <button onclick="previousSong()">Previous</button>
                        <button onclick="addToPlaylist()">Add to Playlist</button>
                        <button onclick="nextSong()">Next</button>
                    </div>
                </div>
            </div>

            <!-- Right Section (Playlists) -->
   <div id="playlistSection">
                <h3>Create Playlist</h3>
                <input type="text" id="playlistInput" placeholder="Enter playlist name">
                <button id="playlistBtn">Create Playlist</button>

   <h3>Current Playlist</h3>
                <ul id="currentPlaylist"></ul>

   <h3>All Playlists</h3>
                <div id="allPlaylists">
                    <!-- Each playlist will show similar to song list -->
                </div>
            </div>
        </div>
    </div>

    <!-- Theme Toggle Button -->
<div id="themeToggle">
        <label class="switch">
            <input type="checkbox" id="themeSwitch">
            <span class="slider round"></span>
        </label>
    </div>

  <script src="script.js"></script>
</body>

</html>
