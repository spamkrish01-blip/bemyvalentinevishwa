# bemyvalentinevishwa
valentines day proposal

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Valentine's Proposal</title>
    <style>
        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
            background-color: #ffcccb;
        }
        .heart {
            position: absolute;
            background: red;
            width: 50px;
            height: 50px;
            clip-path: polygon(50% 0%, 100% 50%, 50% 100%, 0% 50%);
            animation: float 4s infinite;
        }
        @keyframes float {
            0% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
            100% { transform: translateY(0); }
        }
        .note {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 20px rgba(0, 0, 0, 0.5);
            animation: slideIn 1s forwards;
            text-align: center;
        }
        @keyframes slideIn {
            from { transform: translateY(-50px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .buttons {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .yes { background: green; color: white; }
        .no { background: red; color: white; }
        .home-btn { background: #4CAF50; color: white; margin-top: 15px; }
        .cat-image {
            max-width: 100%;
            height: auto;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <div class="heart"></div>
    <div class="note">
        <h1>Will you be my Valentine, Vishwa?</h1>
        <div class="buttons">
            <button class="yes">Yes</button>
            <button class="no">No</button>
        </div>
    </div>
    <script>
        const yesButton = document.querySelector('.yes');
        const noButton = document.querySelector('.no');
        const note = document.querySelector('.note');
        
yesButton.addEventListener('click', function() {
            note.innerHTML = '<h1>Yay! Can\'t wait to celebrate together!</h1><div class="tenor-gif-embed" data-postid="11397231996208728070" data-share-method="host" data-aspect-ratio="1.09211" data-width="100%"><a href="https://tenor.com/view/besito-catlove-gif-11397231996208728070">Besito Catlove GIF</a>from <a href="https://tenor.com/search/besito-gifs">Besito GIFs</a></div> <script type="text/javascript" async src="https://tenor.com/embed.js"><\/script>';
            celebrate();
        });
        
        noButton.addEventListener('click', function() {
            const catImageUrl = 'data:image/jpeg;base64,/9j/4AAQSkZJRgABAQEAYABgAAD/2wBDAAIBAQIBAQICAgICAgICAwUDAwwUAxEAAwwUAwEA...'; // Placeholder - you'll need to add the actual base64 or image URL
            note.innerHTML = '<div style="text-align: center;"><img src="https://imgur.com/your-image-url.jpg" alt="Sad cat meme" class="cat-image" style="max-width: 400px;"><p style="font-size: 24px; margin-top: 20px;">Are you going to say no to me, huh?</p><button class="home-btn" onclick="goHome()">Back to Home</button></div>';
        });
        
        function goHome() {
            location.reload();
        }
        
        function celebrate() {
            for (let i = 0; i < 100; i++) {
                createConfetti();
            }
        }
        
        function createConfetti() {
            const confetti = document.createElement('div');
            confetti.style.position = 'absolute';
            confetti.style.background = 'yellow';
            confetti.style.width = '10px';
            confetti.style.height = '10px';
            confetti.style.left = Math.random() * 100 + 'vw';
            confetti.style.top = Math.random() * 100 + 'vh';
            document.body.appendChild(confetti);
            setTimeout(() => confetti.remove(), 2000);
        }
    </script>
</body>
</html>