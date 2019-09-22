# Portfolio
# Chelsea Love, Coder Academy student

Link to [GitHub](https://github.com/chelseal/stretch-terminal-app)
Link to [Trello](https://trello.com/invite/b/77mUx7cO/7e2b53e2a85f6335203ce3d71da23bb0/t1a2-terminal-application-chelsea-love)
Link to [live website on Netlify](https://chelsea-dev-portfolio.netlify.com)

# Statement of Purpose and Scope

I have built a portfolio website as part of my Coder Academy assessment schedule. It covers 4 section: about, interests, blog and resume. The theme of the portfolio is "Hong Kong night". I chose this theme as I recently visited Hong Kong and found the lights and colours mesmerising. The _target audience_ for my website are the Engineering recruiters of Technology companies.

# Features and Animation

# Feature 1: Gradient
This animation uses pure CSS keyframes to rotate through the colour palette and give the effect of different colours washing over the text.

```css
@keyframes hue {
    0% {
            filter: hue-rotate(0deg);
    }
    100% {
            filter: hue-rotate(-360deg);
    }
}

.viewcv {
    position: fixed;
    top: 50%;
    bottom: 40%;
    right: 50%;
    color: #f326d8;
    animation: hue 15s infinite linear;
    }

.github {
    position: fixed;
    top: 60%;
    bottom: 30%;
    right: 47%;
    color: #f32686;
    animation: hue 15s infinite linear;
    }
```

# Feature 2: Neon flickering sign
This animation uses pure CSS keyframes and pseudo-classes at different intervals along with one to two colours and the colour black to give the effect of a flickering neon sign.

```css
@keyframes neon-flicker-nav-span {

    70% { color: rgba(125, 251, 177, 0.906); }
    72% { color: #333;
        text-shadow: inherit; }
    80% { text-shadow: none; }
    81% { color: rgba(125, 251, 177, 0.906);
        text-shadow: inherit; }
    82% { color: #333;
        text-shadow: none; }
    83% { color: rgba(125, 251, 177, 0.906);
        text-shadow: inherit; }
}

.neon-nav-span {
    position: relative;
    top: 20%;
    width: 10%;
    margin: 0;
    /* padding: 0 20px; */
    color: rgba(125, 251, 177, 0.906);
    text-shadow: 0 0 20px #277526;
    animation: neon-flicker-nav-span linear infinite 2s;
}
    
.neon-nav:after {
    content: attr(data-text);
    position: absolute;
    top: 0;
    left: 0;
    padding: 0 20px;
    z-index: -1;
    color: #43D666;
    filter: blue(15px);
}
    
.neon-nav:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: #277526;
    z-index: -2;
    opacity: 1;
    filter: blur(40px);
}
```

# Feature 3: Carousel of photos
This feature uses a slider frame, animation and images to create a carousel that runs for the user so they can view the photo feature without pressing any buttons.

```css
.slider-frame {
    overflow: hidden;
    height: 400px;
    width: 600px;
    margin-left: 20px;
    margin-right: 20px;
    margin-top: 35%;
}

@keyframes slide_animation {
    0% { left: 0; }
    10% { left: 0; }
    20% { left: 1200px; }
    30% { left: 1200px; }
    40% { left: 2400px; }
    50% { left: 2400px; }
    60% { left: 1200px; }
    70% { left: 1200px; }
    80% { left: 0px; }
    90% { left: 0px; }
    100% { left: 0px; }
}

.slide-images {
    width: 3600px;
    height: 800px;
    margin: 0 0 0 -2400px;
    position: relative;
    animation-name: slide_animation;
    animation-duration: 33s;
    animation-iteration-count: infinite;
    animation-direction: alternate;
    animation-play-state: running;
}

.img-container {
    height: 400px;
    width: 600px;
    position: relative;
    float: left;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

.img-container:nth-of-type(1) {
    background-image: url('images/Amsterdam.jpg');
}
.img-container:nth-of-type(2) {
    background-image: url('images/France.jpg');
}
.img-container:nth-of-type(3) {
    background-image: url('images/AmsterdamBW.jpg');
}
.img-container:nth-of-type(4) {
    background-image: url('images/Aalsmeer.jpg');
}
.img-container:nth-of-type(5) {
    background-image: url('images/Hongkong.jpg');
}
.img-container:nth-of-type(6) {
    background-image: url('images/Porto.jp.jpg');
}
.img-container:nth-of-type(7) {
    background-image: url('images/France2.jpg');
}
.img-container:nth-of-type(8) {
    background-image: url('images/Jarnac.jpg');
}
.img-container:nth-of-type(9) {
    background-image: url('images/LesFrasers.jpg');
}
```

Control Flow Diagram

Please see assessment zip file

# Technology Stack
> HTML
> CSS
> Netlify
