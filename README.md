# 🖐️ Finger Counting AI

A real-time, browser-based hand tracking and finger counting application built with **React**, **Vite**, and **MediaPipe Hands**. This project leverages high-performance computer vision to detect hand landmarks and analyze finger positions with low latency.

![Project Preview](https://via.placeholder.com/800x450.png?text=Finger+Counting+AI+Preview) <!-- Replace with an actual screenshot if available -->

## ✨ Features

- **Real-time Hand Tracking**: Extremely fast and accurate hand landmark detection using MediaPipe.
- **Finger Counting Logic**: Sophisticated algorithm to count extended fingers on one or both hands.
- **Visual Feedback**: Live canvas overlay showing hand skeletals and connection points.
- **Glassmorphism UI**: Modern, sleek, and responsive interface with transparent frosted surfaces.
- **Toggle Camera Controls**: Easy-to-use start/stop functionality for the camera feed.

## 🚀 Tech Stack

- **Frontend**: [React.js](https://reactjs.org/) (Hooks, Functional Components)
- **Build Tool**: [Vite](https://vitejs.dev/)
- **Computer Vision**: [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html)
- **Styling**: Vanilla CSS with Glassmorphism effects

## 📦 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or higher recommended)
- [npm](https://www.npmjs.com/) or [yarn](https://yarnpkg.com/)

### Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sssh72937-ux/Counting-fingers-usig-AI.git
   cd Counting-fingers-usig-AI
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Run the development server**:
   ```bash
   npm run dev
   ```

4. **Open in browser**:
   Navigate to `http://localhost:5173` (or the port shown in your terminal).

## 🛠️ How It Works

### Hand Detection
The application uses the `@mediapipe/hands` solution to extract 21 3D hand landmarks. The `HandTracker.js` utility initializes the tracker and processes each camera frame through a high-performance pipeline.

### Counting Logic
Fingers are counted by comparing the position of the finger tips (e.g., INDEX_FINGER_TIP) relative to their respective MCP (Metacarpophalangeal) joints. 
- **Non-thumb fingers**: If the tip's Y-coordinate is less than the MCP's Y-coordinate (lower Y means higher on screen), the finger is considered "extended".
- **Thumb**: The thumb logic accounts for horizontal movement and handedness (Left vs. Right) to determine extension accurately.

## 🎨 UI Design
The interface is designed with **Glassmorphism** principles:
- `backdrop-filter: blur()` for beautiful transparency.
- Subtle borders and linear gradients.
- Responsive layout that adapts to different screen sizes.

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License
Distributed under the MIT License. See `LICENSE` for more information.

---
Built with ❤️ by [Your Name/GitHub Handle]
