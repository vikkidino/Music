# Music
Download mp3 songs for free
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Music Albums</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', sans-serif;
      background-color: #121212;
      color: #fff;
    }
    header {
      padding: 1rem;
      text-align: center;
      background-color: #1f1f1f;
      font-size: 1.5rem;
    }
    .albums {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 1rem;
      padding: 1rem;
    }
    .album {
      background-color: #1e1e1e;
      border-radius: 8px;
      overflow: hidden;
      cursor: pointer;
      transition: transform 0.2s;
    }
    .album:hover {
      transform: scale(1.03);
    }
    .album img {
      width: 100%;
      height: 200px;
      object-fit: cover;
    }
    .album-title {
      padding: 0.5rem;
      text-align: center;
    }
    .song-list {
      display: none;
      padding: 1rem;
    }
    .song-list.active {
      display: block;
    }
    .song {
      background-color: #292929;
      margin: 0.5rem 0;
      padding: 0.5rem;
      border-radius: 5px;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }
    a.download {
      color: #03a9f4;
      text-decoration: none;
    }
  </style>
</head>
<body>
  <header>🎵 My Music Albums</header>
  <div class="albums">
    <div class="album" onclick="showSongs('album1')">
      <img src="album1.jpg" alt="Album 1">
      <div class="album-title">Movie Album 1</div>
    </div>
    <div class="album" onclick="showSongs('album2')">
      <img src="album2.jpg" alt="Album 2">
      <div class="album-title">Movie Album 2</div>
    </div>
  </div>  <div id="album1" class="song-list">
    <h2>Movie Album 1</h2>
    <div class="song">
      <span>Song 1</span>
      <a href="songs/song1.mp3" download class="download">Download</a>
    </div>
    <div class="song">
      <span>Song 2</span>
      <a href="songs/song2.mp3" download class="download">Download</a>
    </div>
  </div>  <div id="album2" class="song-list">
    <h2>Movie Album 2</h2>
    <div class="song">
      <span>Song A</span>
      <a href="songs/songA.mp3" download class="download">Download</a>
    </div>
    <div class="song">
      <span>Song B</span>
      <a href="songs/songB.mp3" download class="download">Download</a>
    </div>
  </div>  <script>
    function showSongs(albumId) {
      document.querySelectorAll('.song-list').forEach(el => el.classList.remove('active'));
      document.getElementById(albumId).classList.add('active');
      window.scrollTo(0, document.getElementById(albumId).offsetTop);
    }
  </script></body>
</html>
