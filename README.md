# Invoice Processor

This is an Android application that automates the processing of invoice images stored in a specific Google Drive folder. The core functionality revolves around extracting text from these images using Optical Character Recognition (OCR) technology and then populating a Google Sheets spreadsheet with the extracted data.

## Setup

1. Clone this repository to your local machine.
2. Open the project in Android Studio.
3. Sync the project with Gradle files.

## Google Drive and Google Sheets Permissions

1. Go to the Google Cloud Console (https://console.cloud.google.com/).
2. Create a new project or select an existing one.
3. Enable the Google Drive API and Google Sheets API for your project.
4. Create credentials for the APIs.
5. Download the JSON file with your credentials and place it in the `app/src/main/res/raw` directory of the project. Rename it to `credentials.json`.

## Dependencies

This project uses the following dependencies:

- Google Drive API
- Google Sheets API
- Google's Mobile Vision OCR

These are already included in the `build.gradle` file.

## Running the App

1. Build the project in Android Studio.
2. Run the app on an emulator or a connected device.
3. The app will start monitoring the specified Google Drive folder for new invoice images.
4. When a new image is detected, the app will process it using OCR to extract the text.
5. The extracted text will be parsed to identify relevant invoice information.
6. The invoice information will be entered into a Google Sheets spreadsheet.
7. If the invoice already exists in the spreadsheet, the existing row will be updated instead of creating a new one.
8. The processed image file will be moved to a different folder to avoid duplicate processing.

## Error Handling

The app handles errors gracefully and logs them for debugging purposes. Check the `ErrorLogger.java` file for more details.

## Customization

The app allows for easy setup of the Google Drive folder and customization of the spreadsheet format according to user preferences or requirements. Check the `MainActivity.java` and `GoogleSheetsService.java` files for more details.

## Integration

The app offers the flexibility to integrate with various spreadsheet tools or platforms, ensuring broad usability and adaptability in different business contexts. Check the `GoogleSheetsService.java` file for more details.