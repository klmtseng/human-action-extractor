# Human Action Extractor 🏃‍♂️

A web-based tool that uses TensorFlow.js and the MoveNet model to perform real-time human pose estimation on user-uploaded videos. It visualizes the detected skeleton and allows users to extract and download the keypoint data as a JSON file.

**Live Demo:** [**https://klmtseng.github.io/human-action-extractor/**](https://klm.tseng.github.io/human-action-extractor/) 

https://klmtseng.github.io/human-action-extractor/

---

## ✨ Features

-   **Video Upload**: Easily upload any video file from your local machine.
-   **Pose Detection**: Utilizes the lightweight **MoveNet.SinglePose.Lightning** model for fast and efficient skeleton detection.
-   **Real-time Visualization**: Renders the video and the detected skeleton on an HTML canvas.
-   **Data Extraction**: Captures the coordinates and confidence scores of 17 keypoints for each frame.
-   **JSON Export**: Save the extracted time-series skeleton data to a `skeleton_action.json` file with a single click.

---

## 🛠️ Technologies Used

-   **HTML5**: For the core structure of the web page.
-   **Tailwind CSS**: For modern and responsive styling.
-   **JavaScript**: For application logic and interactivity.
-   **TensorFlow.js**: An open-source library for machine learning in JavaScript.
-   **TensorFlow.js Models (Pose Detection)**: Specifically, the **MoveNet** model for pose estimation.

---

## 🚀 How to Use

1.  **Open the Web App**: Navigate to the live demo link.
2.  **Select a Video**: Click the "Select Video" button and choose a video file containing a person.
3.  **Process the Video**: Click "Detect & Extract Action" to begin processing. The tool will play the video and draw the detected skeleton in real-time.
4.  **Save the Data**: Once processing is complete, click "Save Skeleton Data" to download the keypoints in JSON format.

---

## 📂 Output JSON Structure

The output JSON is an array of objects, where each object represents a frame in the video.

```json
[
  {
    "timestamp": 0.033333,
    "keypoints": [
      { "y": 133, "x": 330, "score": 0.95, "name": "nose" },
      { "y": 135, "x": 335, "score": 0.92, "name": "left_eye" },
      // ... 15 more keypoints
    ]
  },
  {
    "timestamp": 0.066666,
    "keypoints": [
      // ... keypoints for the next frame
    ]
  }
]
