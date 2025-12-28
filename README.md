# (Github) Pages Audio Player

A simple, user-friendly web-based audio player for motivational audio files, hosted on GitHub Pages.

## Features

- **Automatic Audio Detection**: Dynamically loads all audio files from the `assets/` folder using GitHub API
- **Multiple Format Support**: Supports MP3, WAV, OGG, M4A, and AAC audio formats
- **Scrollable Interface**: Clean, responsive design with scrollable audio list for many files
- **Full Audio Controls**: Play/pause, volume control, progress bar with seeking, and loop toggle
- **No Favicon Errors**: Optimized to prevent unnecessary 404 requests

## Quick Start

1. **Clone the Repository**
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO_NAME.git
   cd YOUR_REPO_NAME
   ```

2. **Add Your Audio Files**
   - Place your audio files in the `assets/` folder
   - Supported formats: MP3, WAV, OGG, M4A, AAC

3. **Configure the Repository**
   - In `index.html`, update the `owner` and `repo` variables in the JavaScript with your GitHub username and repository name
   - Ensure your repository is **public** (required for GitHub API access)

4. **Deploy to GitHub Pages**
   - Push your changes to GitHub
   - Go to repository Settings → Pages
   - Select "Deploy from a branch" and choose your main branch
   - Your site will be available at `https://YOUR_USERNAME.github.io/YOUR_REPO_NAME/`

## How It Works

The audio player automatically:
- Fetches the list of files in the `assets/` folder via GitHub API
- Filters for supported audio formats
- Creates individual audio players for each file
- Uses the filename (without extension) as the title, with underscores replaced by spaces

## Adding More Audio Files

Simply add new audio files to the `assets/` folder and push to GitHub. The page will automatically detect and display them on the next load.

## Browser Support

Works in all modern browsers that support:
- HTML5 Audio
- Fetch API
- ES6 JavaScript

## Customization

- **Styling**: Modify the CSS in `index.html` to change colors, fonts, or layout
- **Audio Types**: Add more extensions to the `audioExtensions` array in the JavaScript
- **Title Formatting**: Adjust the `createAudioPlayer` function to customize how titles are generated

## Troubleshooting

- **No Audio Files Showing**: Ensure your repository is public and the `owner`/`repo` variables are correct
- **CORS Errors**: This is normal in local development; it works on GitHub Pages
- **Audio Not Playing**: Check that your audio files are in supported formats and properly encoded

