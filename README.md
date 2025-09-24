# Workout Timer

A simple, single-file HTML, CSS, and JavaScript web page that provides a highly configurable workout timer. It's designed to be used directly in your web browser without the need for a server or complex setup, making it perfect for quick, personalized workouts.

## Live Demo

You can try the timer live right now\!

[**View the Timer on GitHub Pages**](https://www.google.com/search?q=https://bumbarashka.github.io/workout-timer/index.html)

## Features

  * **Configurable Parameters**: Easily set the total workout time ($T$), the number of exercises ($N$), and an initial delay ($D$) using input fields.
  * **Initial Delay Countdown**: Provides a "Get Ready" screen with a countdown to allow you to prepare before the workout begins.
  * **Dual Timers**: Features a primary, prominent countdown for the current exercise interval and a secondary timer for the total workout duration.
  * **Audio Alerts**: A distinct beep sound signals the beginning of each new exercise interval.
  * **Pause & Resume**: Offers a simple interface to pause and resume the workout at any point.
  * **Workout Completion Summary**: After the workout ends, a clear summary is displayed showing the total time and number of exercises completed.
  * **Prevents Screen Dimming**: Uses the browser's **Wake Lock API** to ensure your screen remains on and active while the timer is running, preventing interruptions from power-saving modes.

## How to Use

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/bumbarashka/workout-timer.git
    ```
2.  **Open the File**:
    Simply open the `index.html` file in any modern web browser (like Chrome, Firefox, or Safari). No internet connection is needed after the initial download.
3.  **Set Your Workout**:
      * **Total Time (T)**: Enter the total duration of your workout in minutes.
      * **Number of Exercises (N)**: Enter how many exercises you will do in that time.
      * **Initial Delay (D)**: Set a preparation time in seconds to allow you to get ready.
4.  **Start the Timer**:
    Click the **Start Workout** button to begin the countdown.

## Technical Details

The timer is built with pure web technologies and relies on a few key concepts for its advanced functionality:

  * **Milestone-based Logic**: The JavaScript code calculates an array of "milestone" seconds for each exercise change. This approach guarantees that each exercise interval is an equal length, even when the total time is not perfectly divisible by the number of exercises (e.g., $T=20$ minutes and $N=90$ exercises).
  * **Dynamic UI**: The user interface adapts based on the timer's state, showing configuration options, a delay countdown, the main timer display, or a completion message as needed.
  * **Wake Lock API**: This modern browser API is used to programmatically request a "wake lock" for the screen. This is a robust and power-efficient way to prevent the screen from dimming or locking during the workout.

-----

## Contributing

If you find a bug, have a feature request, or want to contribute to the code, feel free to open an issue or submit a pull request. Contributions are welcome\!
