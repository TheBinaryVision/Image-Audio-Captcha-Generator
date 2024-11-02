# CAPTCHA Generator

This project is a CAPTCHA generator that creates both audio and image CAPTCHAs using Python's `tkinter` for the GUI, `captcha` for image generation, and `pyttsx3` for text-to-speech audio generation.

## Features

- Generates random alphanumeric image CAPTCHAs.
- Generates audio CAPTCHAs using randomly generated digits.
- GUI interface for easy interaction.
- Options to regenerate CAPTCHAs.

## Requirements

To run this project, you need to install the following Python packages:

- `tkinter` (usually included with Python)
- `captcha`
- `pyttsx3`

## Installation

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/TheBinaryVision/Image_Audio_Captcha_Generator.git
   ```

2. Navigate to the project directory:

   ```bash
   cd Image_Audio_Captcha_Generator
   ```

3. Install the required packages. You can use `pip`:

   ```bash
   pip install captcha pyttsx3
   ```

## Usage

1. Run the application:

   ```bash
   python3 Captcha.py
   ```

2. The GUI will open, allowing you to interact with it to generate audio and image CAPTCHAs.

3. Click the "Show Image" button to display the image CAPTCHA, and "Play Audio" to hear the audio CAPTCHA.

4. Enter the CAPTCHA values into the respective entry fields and click "Check" to verify your input.

## Code Overview

The code is structured into several key functions, each responsible for a specific part of the CAPTCHA generation process:

- **`generate_captcha()`**: 
  - Generates a random string consisting of 6 alphanumeric characters (both letters and digits).
  - Ensures that each character is unique by removing it from the data set once selected.

- **`generate_digit_captcha()`**: 
  - Generates a 4-digit string for the audio CAPTCHA.
  - Returns the digits formatted as a string with spaces for better clarity in audio playback.

- **`generate_image_captcha()`**: 
  - Opens the generated CAPTCHA image file (`c1.png`) using the default image viewer.

- **`generate_first_image()`**: 
  - Generates the initial image CAPTCHA using the `ImageCaptcha` class from the `captcha` library.
  - Calls `generate_captcha()` to get a random string and writes it to an image file.

- **`regenerate_image_captcha()`**: 
  - Similar to `generate_first_image()`, but specifically used to regenerate and display a new image CAPTCHA upon request.

- **`generate_audio_captcha()`**: 
  - Uses the `pyttsx3` library to convert the digit CAPTCHA into audio.
  - Configures the voice and speaking rate of the text-to-speech engine before playback.

- **`regenerate_audio_captcha()`**: 
  - Calls `generate_audio_captcha()` to create a new audio CAPTCHA.

- **`check_audio_captcha()`** and **`check_image_captcha()`**: 
  - Validate user input against the generated CAPTCHAs.
  - Provide feedback via message boxes indicating whether the input matches the expected value.

## GUI Layout

The user interface is created using `tkinter` and consists of:

- A title frame displaying the application name.
- Separate sections for audio and image CAPTCHA, each with buttons for generation and checking.
- Entry fields for user input corresponding to both audio and image CAPTCHAs.

## Contribution

Feel free to contribute to this project by creating issues or submitting pull requests. You can enhance functionality, improve the GUI, or add new features.
