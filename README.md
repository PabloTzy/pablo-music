# Pablo Music

A simple Node.js module to search and download music from YouTube. With `pablo-music`, you can easily play and retrieve music tracks using a search query.

## Features

- Search for music on YouTube.
- Download audio in MP3 format.
- Simple and easy-to-use API.

## Installation

You can install the `pablo-music` module via npm:

```bash
npm install pablo-music
```

## Usage

To use the `pablo-music` module, require it in your Node.js application and call the `playMusic` function with a search query.

### Example

```javascript
const { playMusic } = require('pablo-music');

(async () => {
  const musicInfo = await playMusic('Your Favorite Song');
  if (musicInfo) {
    console.log('Music Info:', musicInfo);
  } else {
    console.log('Music not found or failed to download.');
  }
})();
```

### Parameters

- `query` (string): The search query for the music you want to find.

### Returns

The `playMusic` function returns a Promise that resolves to an object containing:

- `title` (string): The title of the music.
- `duration` (string): The duration of the music.
- `mp3` (string): The direct URL to download the music in MP3 format.
- `thumbnail` (string): The URL of the music thumbnail.
- `views` (string): The number of views for the video.
- `uploaded` (string): The time since the video was uploaded.

## Error Handling

If the function fails to find any results or download the music, it will log the error to the console and return `null`.

## Contributing

Contributions are welcome! If you would like to contribute to this project, please fork the repository and submit a pull request.

## License

This project is licensed under the ISC License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [yt-search](https://www.npmjs.com/package/yt-search) - For searching YouTube videos.
- [Axios](https://axios-http.com/) - For making HTTP requests.
