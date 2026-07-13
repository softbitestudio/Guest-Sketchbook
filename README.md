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
