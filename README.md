# Project
# Instagram Stories Clone — 24-Hour Ephemeral Stories

## 📌 Project Overview

The Instagram Stories Clone is a browser-based web application that recreates the core experience of Instagram Stories. It allows users to upload images, add captions, view stories in a full-screen interface, navigate between stories, and automatically remove expired stories after 24 hours.

The application uses client-side storage to retain stories in the browser and includes a time simulation feature for testing story expiration without waiting an entire day.

## ✨ Features

- **Image Upload:** Upload images from your device to create stories.
- **Image Compression:** Resize uploaded images to fit within 1080 × 1920 pixels while maintaining their aspect ratio.
- **Story Captions:** Add captions of up to 80 characters.
- **24-Hour Expiration:** Automatically remove stories that are 24 hours old or older.
- **Story Viewer:** View stories in a full-screen interface.
- **Automatic Playback:** Stories advance automatically after five seconds.
- **Story Navigation:** Navigate between stories using on-screen controls, keyboard keys, and touch gestures.
- **Pause and Resume:** Pause story playback by holding the viewer and resume when released.
- **Story Deletion:** Delete an individual story from the viewer.
- **Persistent Browser Storage:** Store story information locally using `localStorage`.
- **Expiration Countdown:** Display the elapsed time and remaining time before a story expires.
- **Time Travel Simulator:** Advance simulated time by 12 or 24 hours to test expiration behavior.
- **Storage Statistics:** Display an estimate of the storage used by saved stories.
- **Responsive Interface:** Provide a mobile-oriented interface that adapts to different screen sizes.
- **Preloaded Stories:** Include predefined stories to demonstrate the interface when the browser storage is empty.

## 🛠️ Technologies Used

- **HTML5:** Structures the application interface.
- **Tailwind CSS:** Provides utility-based styling and responsive layouts through the CDN.
- **JavaScript (ES6+):** Implements story creation, navigation, timers, expiration, and storage management.
- **Browser Local Storage:** Persists story data between page reloads.
- **Canvas API:** Resizes and compresses uploaded images.
- **File API:** Reads image files selected by the user.
- **Font Awesome 6.4.0:** Provides interface icons.
- **CSS Animations:** Adds transitions and story appearance effects.

## 📂 Project Structure

```text
instagram-stories-clone/
├── ig.html       # Main application containing HTML, CSS, and JavaScript
└── README.md     # Project documentation
```

The application logic and styling are included within the HTML file, so separate CSS and JavaScript files are not required.

## ⚙️ Prerequisites

Before running the application, ensure that you have:

- A modern web browser, such as Google Chrome, Mozilla Firefox, or Microsoft Edge.
- An internet connection to load Tailwind CSS, Font Awesome, and externally hosted story images.
- A local copy of the project file.

No backend server, database installation, or package manager is required for basic local use.

## 🚀 Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
```

Replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your GitHub username and repository name.

### 2. Navigate to the project directory

```bash
cd YOUR-REPOSITORY
```

### 3. Open the application

Open `ig.html` in your preferred web browser.

Alternatively, open the project folder in Visual Studio Code and use the Live Server extension to launch the application locally.

## ▶️ How to Use

1. Open the application in your browser.
2. Click **Your story** to select an image from your device.
3. Preview the image and add an optional caption.
4. Click **Share Story** to publish it.
5. Select a story from the horizontal story tray to open the full-screen viewer.
6. Navigate between stories using the left and right tap areas, keyboard controls, or touch gestures.
7. Use the delete icon to remove the currently displayed story.
8. Open **Time Travel** to simulate the passage of time and test expiration.
9. Observe the active story count and expiration countdown.

## ⏳ Story Expiration Logic

Each story records a creation timestamp. The application compares this timestamp with the current time to determine whether the story is still valid.

- Stories younger than 24 hours remain active.
- Stories that reach or exceed 24 hours are removed during expiration checks.
- Expiration checks run periodically, every 10 seconds.
- The Time Travel controls allow simulated time advancement to test expiration behavior.

The expiration mechanism operates within the browser application and does not depend on a backend service.

## 💾 Data Storage

The application uses the browser's `localStorage` to store story data, including timestamps, captions, image data, and usernames.

**Important limitations:**
- Stories are stored locally in the browser rather than in a central database.
- Data is not automatically synchronized across different browsers or devices.
- Clearing the browser's site data can remove saved stories.
- Browser storage quotas may limit the number or size of images that can be stored.

## 🧪 Testing Story Expiration

The application includes a built-in Time Travel panel for testing expiration behavior.

1. Click **Time Travel** in the application header.
2. Select **+12 Hours Warp** to advance simulated time by 12 hours.
3. Select **+24 Hours Warp (Expire All)** to advance simulated time by 24 hours.
4. Use **+ Inject 25hr Old Story** to test the removal of an already-expired story.
5. Use **Reset Clock** to reset the simulated time offset.
6. Use **Reset Storage** to clear the stored stories and reset the simulation.

These controls make it possible to test the expiration mechanism quickly.

## 🔗 Project Links

- **GitHub Repository:** https://github.com/Tejas-source-web/Project
- **Project Page:** https://roadmap.sh/projects/stories-feature
- **Live Application:**  https://tejas-source-web.github.io/Project/

## 🔮 Future Improvements

- Add support for video stories.
- Implement user authentication and individual user profiles.
- Introduce a backend API and database for persistent, cross-device storage.
- Add story privacy settings and audience controls.
- Implement reactions and functional replies.
- Improve image upload validation and error handling.
- Add automated tests for expiration and navigation behavior.
- Improve accessibility and provide additional keyboard controls.

## 📄 License

No license has been specified for this project. Add a `LICENSE` file and identify the applicable license before distributing the project under specific reuse terms.

## 👤 Author

**Tejas**

- GitHub: https://github.com/YOUR-USERNAME
