# two-frames-image
two frames image - no mint
Step-by-Step Guide
HTML Structure: Create a single index.html file with JavaScript to handle frame navigation.
Image Display: Ensure the images maintain a 1:1 ratio.
Buttons: Add buttons to navigate between frames.
index.html
html
Αντιγραφή κώδικα
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Warpcast Frame</title>
    <style>
        body { font-family: Arial, sans-serif; display: flex; flex-direction: column; align-items: center; justify-content: center; height: 100vh; margin: 0; }
        .frame { display: none; flex-direction: column; align-items: center; }
        .frame.active { display: flex; }
        img { width: 100%; max-width: 300px; aspect-ratio: 1 / 1; object-fit: cover; }
        button { margin-top: 20px; padding: 10px 20px; font-size: 16px; }
    </style>
</head>
<body>
    <div id="frameOne" class="frame active">
        <h1>One</h1>
        <img src="https://aquamarine-elegant-meerkat-268.mypinata.cloud/ipfs/Qmdo6eeTUfnGE39ofKNAtaKnkKyZbromBKPAVKm5qXbPhY" alt="One">
        <button onclick="showFrame('frameTwo')">Next</button>
    </div>
    <div id="frameTwo" class="frame">
        <h1>Two</h1>
        <img src="https://aquamarine-elegant-meerkat-268.mypinata.cloud/ipfs/QmRDjBgQDWERxwLDtCUU95BZrYw5gpEzx3Tu3h5AYb5vCR" alt="Two">
        <button onclick="showFrame('frameOne')">Back</button>
    </div>
    <script>
        function showFrame(frameId) {
            document.querySelectorAll('.frame').forEach(frame => {
                frame.classList.remove('active');
            });
            document.getElementById(frameId).classList.add('active');
        }
    </script>
</body>
</html>
Instructions to Deploy
Create a Repository: Create a new repository on GitHub and add the index.html file.
Deploy on Vercel:
Sign in to Vercel and create a new project.
Import your GitHub repository.
Deploy the project and get the public URL.
Validate with Warpcast: Use the public URL from Vercel in the Warpcast validator.
Steps:
Add the index.html to your repository: Follow the previous instructions to add the file to your GitHub repository.
Deploy on Vercel: Vercel will automatically detect the changes and redeploy your project.
Validate and Embed: Use the public URL from Vercel in the Warpcast validator.
This HTML file will create a simple interactive Frame with two views, allowing users to navigate between "One" and "Two" with the provided images.


