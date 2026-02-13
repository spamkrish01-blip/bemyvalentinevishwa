```javascript
// Existing yesButton click event listener
yesButton.addEventListener('click', function() {
    const celebrationMessage = 'Happy Valentine\u2019s Day!';
    innerHTML = celebrationMessage;
    // Insert Tenor GIF embed
    const gifEmbed = `\n<div class=\"tenor-gif-embed\">\n    <a href=\"https://tenor.com/view/thank-you-lovers-romantic-gif-18234866\">\n        <img src=\"https://media.tenor.co/images/83c09b4b177a7ba32b94d116e0474919/raw.gif\" alt=\"Thank You Lovers Romantic GIF\" />\n    </a>\n</div>\n<script type=\"text/javascript\" async src=\"https://tenor.com/embed.js\"></script>\n`;
    innerHTML += gifEmbed;
});
```