☕ Chai Tapri
A cozy digital chai tapri for the internet — a minimal, immersive music experience where you can sit back, listen to nostalgic Hindi songs, and enjoy an animated chai-stall atmosphere.
✨ Features
🎥 Animated fullscreen background — immersive MP4/WebM background video.
🎵 YouTube-powered music player — play songs directly through the YouTube IFrame API.
📜 36-song playlist — curated mix of nostalgic Hindi songs.
▶️ Play / Pause controls
⏭️ Next / Previous song
🔀 Shuffle mode
🔁 Loop mode
🔊 Volume control & mute
📊 Live progress bar with seek support.
🎚️ Animated equalizer while music is playing.
👥 Real-time listener counter using Firebase Realtime Database.
📱 Responsive design for desktop and mobile.
🔗 Share Link functionality.
𝕏 Share to X functionality.
🌙 Dark, glassmorphism-inspired interface.
🛠️ Tech Stack
HTML5
Tailwind CSS
JavaScript
YouTube IFrame Player API
Firebase Realtime Database
Google Fonts
MP4/WebM Video
📁 Project Structure
chai-tapri/
│
├── index.html
├── bg.mp4
├── bg.webm
├── firebase-config.js
└── README.md
🎬 Background Video
The site uses a fullscreen HTML5 video:
HTML
<video
  id="bgVideo"
  autoplay
  loop
  muted
  playsinline
>
  <source src="bg.mp4" type="video/mp4">
  <source src="bg.webm" type="video/webm">
</video>
The background video is intentionally kept independent from the YouTube music player.
Changing, pausing, or switching songs should not control the background video.
🎵 Music Player
Music playback uses the YouTube IFrame API.
The YouTube player is placed off-screen so that the custom Chai Tapri interface can control it.
Chai Tapri UI
      │
      ├── Background Video
      │      └── bg.mp4 / bg.webm
      │
      └── Music Player
             └── YouTube IFrame API
🔥 Firebase
Firebase Realtime Database is used for the live listener counter.
Listeners are temporarily registered under:
live_listeners
When a user disconnects, Firebase automatically removes their presence entry using onDisconnect().
Make sure your Firebase configuration is correctly configured before deploying.
🚀 Getting Started
1. Clone the repository
git clone YOUR_REPOSITORY_URL
cd chai-tapri
2. Add your background
Place your video files in the project root:
bg.mp4
bg.webm
3. Configure Firebase
Make sure your Firebase configuration is available through:
firebase-config.js
4. Run locally
Because YouTube playback and some browser media policies can behave differently on file://, use a local server.
For example:
npx serve .
or use VS Code Live Server.
5. Deploy
The project can be deployed as a static website using platforms such as Vercel, Netlify, or GitHub Pages.
⚠️ Important Notes
YouTube playback
Some YouTube videos may be unavailable because of:
Regional restrictions
Copyright restrictions
Embedded playback restrictions
YouTube policy changes
The player automatically handles playback errors and can move to another track when appropriate.
Background video autoplay
The background video is:
muted
autoplay
loop
playsinline
These attributes improve compatibility with browser autoplay policies.
🎨 Design Philosophy
Chai Tapri is designed around the feeling of:
"Just sit here for a while."
The interface intentionally stays minimal so that the background atmosphere + music remain the main experience.
Inspired by the aesthetic of viral experimental web experiences — simple interaction, strong atmosphere, nostalgia, and a little bit of internet weirdness.
📱 Responsive
The UI adapts to different screen sizes:
📱 Mobile
📲 Tablet
💻 Desktop
The player remains centered near the bottom of the screen while the background fills the entire viewport.
🔮 Future Ideas
🎧 Multiple playlists — Morning / Afternoon / Night
🌧️ Weather-based backgrounds
☕ Chai brewing animation
🪑 Interactive tapri elements
💬 Anonymous chai conversations
🌃 Time-based background scenes
🎙️ Radio-style voice announcements
📻 Retro radio mode
❤️ Favorite songs
🔥 Song listening streak
🌍 Global listener map
🤝 Contributing
Contributions, ideas, and improvements are welcome.
Fork the repository.
Create a feature branch.
git checkout -b feature/amazing-feature
Commit your changes.
git commit -m "Add amazing feature"
Push the branch.
git push origin feature/amazing-feature
Open a Pull Request.
📄 License
This project is intended as a personal/experimental web project.
Music and video content played through YouTube remains subject to the respective rights holders and YouTube's terms.
�

☕ यहाँ चाय, दोस्ती और किस्से मिलते हैं
Made with chai & code. ❤️