# Guest-Sketchbook
website visitors can leave a drawing instead of text.

# Single Canvas Guest Sketchbook

A lightweight, multiplayer digital guestbook built with plain HTML, CSS, and JavaScript. Instead of leaving text, visitors can draw a picture. When a user submits a new drawing, it overwrites the previous one on the server, saving space and creating a living, constantly changing canvas.

It uses [JSONBin.io](https://jsonbin.io/) as a free, serverless database to store the image data.

## Prerequisites

You do not need a traditional backend or database for this project. You only need a free JSONBin account.

1. Go to [JSONBin.io](https://jsonbin.io/) and sign up for a free account.
2. In your dashboard, click **Create New Bin**.
3. In the empty JSON editor, type exactly this:
   ```json
   {
     "image": ""
   }
`

Click Save.

    Copy your Bin ID (found in the URL or the Bin details).

    Go to API Keys (in the sidebar) and copy your Master Key.

Setup Instructions

    Download or copy the index.html file in this repository.

    Open index.html in any code editor (VS Code, Notepad, etc.).

    Scroll down to the <script> section near the bottom.

    Locate these two lines:
    JavaScript

   ```
 const BIN_ID = 'YOUR_BIN_ID_HERE'; 
    const API_KEY = 'YOUR_API_KEY_HERE';
`
    Replace YOUR_BIN_ID_HERE with the Bin ID you copied.

    Replace YOUR_API_KEY_HERE with your Master Key.

    **Save the file**.

__How to Run__

Because this is a plain HTML file, you can test it immediately by double-clicking the index.html file to open it in your browser.

To take it live, simply upload the index.html file to your web host (GitHub Pages, Netlify, Vercel, or any standard cPanel hosting).
How it Works

    Drawing: Uses the HTML5 <canvas> element to capture mouse and touch movements.

    Saving: Converts the canvas drawing into a Base64 text string (canvas.toDataURL).

    Backend: Sends a PUT request to JSONBin to overwrite the existing text string with the new one.

    Loading: Sends a GET request to JSONBin when the page loads to fetch and display the most recent drawing.
