<!-- .slide: data-background="media/img/aframe.jpg" -->

<div class="talk-title">
  <h1>Hacking the A-Frame</h1>
  <p>A workshop using A-Frame to develop VR Experiences</p>
  <p class="talk-info">
    @infil00p | | phonegap.com
  </p>
</div>

<!-- NOTES -->
- A Frame is by Mozilla VR
- A Frame works with Cordova
- Onboard web developers into the 3D and VR world with easy-to-use tools
- Prototype WebVR experiences faster

------

# Virtual Reality

<!-- .slide: data-background-video="media/video/virtualreality.mp5" data-background-video-loop="true" data-background-video-muted="true" data-state="state--bg-dark" -->

<!-- NOTES -->
- Ask how many have tried VR.
- Virtual reality is a technology platform that transports you to realistic, interactive, immersive 3D environments
- It's the next platform, will change how we work + play + communicate digitally, face of society

---

<div class="image-row">
  <div><img data-src="media/img/google-cardboard.png"></div>
  <div><img data-src="media/img/google-daydream.png"></div>
  <div><img data-src="media/img/samsung-gearvr.png"></div>
</div>

<div class="image-row">
  <div><img data-src="media/img/oculus-rift.png"></div>
  <div><img data-src="media/img/playstation-vr.png"></div>
  <div><img data-src="media/img/htc-vive.png"></div>
</div>

<!-- NOTES -->
- Backed by the largest corporations in the world, everyone wants in
- Range from cheap to expensive, tethered and untethered, controllers, tracking
- HTC Vive with Steam currently offers the most compelling experiences, but never know
- See a lot of different devices, systems, platforms competing against each other...

---

## Friction of VR Ecosystems

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/gatekeeper.png">
    <i>Gatekeepers</i>
  </div>
  <div>
    <img data-src="media/img/downloads-installs.png">
    <i>Installs</i>
  </div>
  <div>
    <img data-src="media/img/closed-door.png">
    <i>Closed</i>
  </div>
</div>

<!-- NOTES -->
- App stores and corporations control distribution: can take down or block content
- Downloads / installs are a barrier to consumption: small business pages
- Closed ecosystem: proprietary engines, steep learning curves, siloed experiences, fragmentation
- We want VR to be successful, so we want a platform without these points of friction. The answer is WebVR...

------

# WebVR

An open virtual reality platform with the advantages of **the Web**

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/web-is-open.png">
    <i>Open</i>
  </div>
  <div>
    <img data-src="media/img/web-is-connected.png">
    <i>Connected</i>
  </div>
  <div>
    <img data-src="media/img/web-is-instant.png">
    <i>Instant</i>
  </div>
</div>

<!-- NOTES -->
WebVR is...virtual reality in the browser, powered by the Internet

Open:
- Anyone can publish
- Open source culture with open standards

Connected:
- Traverse worlds

Instant:
- Click a link on Twitter or Weibo, immediate VR experiences
- No installs
- Imagine for long tail experiences: shopping & personal spaces
- Great for long tail bite-sized experiences

Transition:
- Web has advantages that make it the best platform for the people
- Need to act to make it reality, can't wait for VR to bake and crystallize
- Get involved

---

<img class="stretch" data-src="media/img/webvr.png">

Browser APIs that enable WebGL rendering to headsets and access to VR
sensors

https://w3c.github.io/webvr/

<!-- NOTES -->
API:
- Optimized rendering path to headsets
- Access position and rotation (pose) data

History:
- Initial WebVR API by Mozilla
- Working W3C community group
- Mozilla, Google, Samsung, Microsoft, community currently iterating WebVR 1.0 API

Not just a specification, it's implemented...

---

https://webvr.rocks

<div class="captioned-image-row small">
  <div>
    <img data-src="media/img/firefox-nightly.png">
    <i>Firefox Nightly</i>
  </div>
  <div>
    <img data-src="media/img/edge.jpg">
    <i>Microsoft Edge</i>
  </div>
  <div>
    <img data-src="media/img/chromium.png">
    <i>Chromium</i>
  </div>
</div>

<div class="captioned-image-row small">
  <div>
    <img data-src="media/img/chrome.jpg">
    <i>Chrome for Android</i>
  </div>
  <div>
    <img data-src="media/img/carmel.jpg">
    <i>Oculus Carmel</i>
  </div>
  <div>
    <img data-src="media/img/samsung-browser.png">
    <i>Samsung Internet</i>
  </div>
  <div>
    <img data-src="media/img/google-cardboard.png">
    <i>Mobile Polyfill</i>
  </div>
</div>

<!-- NOTES -->
- Firefox + Chrome WebVR 1.0 hits release channels by early 2017
- Currently behind Nightly, custom builds, and flags
- Mobile Polyfill: use device motion / orientation sensors to polyfill on smartphones
- With all the browsers behind it...

---

Too hard to create WebVR experiences...

---

<!-- .slide: data-background-video="media/video/boilerplate.mp4" data-state="state--bg-dark" -->

<div class="slide__boilerplate">
  <p>Import WebVR polyfill</p>
  <p>Set up camera</p>
  <p>Set up lights</p>
  <p>Initialize scene</p>
  <p>Declare and pass canvas</p>
  <p>Listen to window resize</p>
  <p>Install VREffect</p>
  <p>Instantiate renderer</p>
  <p>Create render loop</p>
  <p>Preload assets</p>
  <p>Figure out responsiveness</p>
  <p>Deal with metatags and mobile</p>
</div>

<!-- NOTES -->
- It's still too difficult to create WebVR experiences
- Huge obstacle if doing small prototypes and experiments
- Boilerplate needs updating with new versions of WebVR, three.js, and browser quirks
- Encapsulate all of that into one line...

------

# A-Frame

<!-- .slide: data-background="media/img/aframe-rendered-full.png" -->

A web framework for building virtual reality experiences

<!-- NOTES -->
- Launched last December
- Why:
  - Easy for web developers to create VR content, without graphics knowledge
  - Prototype and experiment WebVR and VR UX faster
  - Vehicle to kickstart WebVR ecosystem

---
<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 0: Prep

<ul>
  <li>Did you bring a laptop? GOOD!</li>
  <li>Did you bring a phone that's not the Moto X Play?</li>
  <li>Do you have a USB Cable? AWESOME!!!</li>
  <li>You have a cardboard</li>
</ul>

---
<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 1: Use the source

<ul>
  <li> Grab the following source:</li>
  <li> (If the Internet goes down, we have USB Keys)</li>
  <li> Modify the index.html </li>
</ul>

---
## Step 1: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```html
        <img id="bridal-falls" src="images/Bridal_Falls.jpg">
        <img id="bridal-falls-thumb" src="images/Bridal_Falls_Thumb.jpg">
        <img id="dinosaur" src="images/Dinosaur.jpg">
        <img id="dinosaur-thumb" src="images/Dinosaur_Thumb.jpg">
        <img id="nexen" src="images/Nexen_Beach.jpg">
        <img id="nexen-thumb" src="images/Nexen_Thumb.jpg">
        <img id="sundance" src="images/Sundance.jpg">
        <img id="sundance-thumb" src="images/Sundance_Thumb.jpg">
```
<!-- .element: class="stretch" -->

<!-- NOTES -->
- Just HTML
- Drop a script tag, no build steps
- Using Custom HTML Elements
- One line of HTML `<a-scene>` handles
  - canvas, camera, renderer, lights, controls, render loop, WebVR polyfill, VREffect
- Put stuff inside our scene...

---
## Step 1: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```html
      <!-- Image links. -->
      <a-entity id="links" layout="type: line; margin: 1.5" position="0 -1 -4">
        <a-entity template="src: #link" data-title="Dinosaur Provincial Park" data-src="#dinosaur" data-thumb="#dinosaur-thumb"></a-entity>
        <a-entity template="src: #link" data-title="Bridal Falls" data-src="#bridal-falls" data-thumb="#bridal-falls-thumb"></a-entity>
        <a-entity template="src: #link" data-title="Nexen Beach" data-src="#nexen" data-thumb="#nexen-thumb"></a-entity>
        <a-entity template="src: #link" data-title="Sundance, Utah" data-src="#sundance" data-thumb="#sundance-thumb"></a-entity>
      </a-entity>
```
<!-- .element: class="stretch" -->

<!-- NOTES -->
- Just HTML
- Drop a script tag, no build steps
- Using Custom HTML Elements
- One line of HTML `<a-scene>` handles
  - canvas, camera, renderer, lights, controls, render loop, WebVR polyfill, VREffect
- Put stuff inside our scene...

---

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 2: Let's add some more UI

<ul>
  <li> Create a plane </li>
  <li> Add some buttons </li>
  <li> Try and do some layout </li>
</ul>

---
## Step 2: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```html
      <a-entity id="container" position="0 -1 -4"
        geometry="primitive: plane; height: 2; width: 5"
        material="color: #000000" >
        <a-entity id="left" class="link" position="-2 -0.6 0.2" 
                  geometry="primitive: plane; height: 0.3; width: 0.3"
                  scrollleft="on: click"
                  material="shader: flat; src: #left"></a-entity>
        <a-entity id="right" class="link" position="2 -0.6 0.2" 
                  geometry="primitive: plane; height: 0.3; width: 0.3"
                  scrollright="on: click"
                  material="shader: flat; src: #right"></a-entity>
        <a-entity id="links" layout="type: line; margin: 1.5" position="0 0.2 0.2">
            <a-entity template="src: #link" data-title="Dinosaur Provincial Park" data-src="#dinosaur" data-thumb="#dinosaur-thumb"></a-entity>
            <a-entity template="src: #link" data-title="Bridal Falls" data-src="#bridal-falls" data-thumb="#bridal-falls-thumb"></a-entity>
            <a-entity template="src: #link" data-title="Nexen Beach" data-src="#nexen" data-thumb="#nexen-thumb"></a-entity>
            <a-entity template="src: #link" data-title="Sundance, Utah" data-src="#sundance" data-thumb="#sundance-thumb"></a-entity>
          </a-entity>
      </a-entity>

```
<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening
---
## Step Two: Inspector

<!-- .slide: data-background="media/img/inspector.png" data-state="state--bg-dark" -->

Visual tool for A-Frame. Just `<ctrl>+<alt>+i`.

<div class="stretch" data-aframe-scene="scenes/80s.html"></div>

---

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 3: Wire up the Components

<ul>
  <li> Create a new JS file</li>
  <li> Use the entity-component system</li>
  <li> Get some things moving </li>
</ul>

---
## Step 3: Wiring up the components

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```javascript
AFRAME.registerComponent('scrollleft', {
  schema: {
    on: { type: 'string' }
  },
  init: function()  {
    this.el.addEventListener(this.data.on, this.scroll);
  },
  scroll: function()
  {
    console.log("This should fire");
    //The current position is what we're modifying
    var links = document.querySelector("#links");
    var layout = links.getAttribute('layout');
    var position = links.getAttribute('position');
    var maxLeft =  -(layout.margin * layout.columns);
    if(position.x != maxLeft) {
      position.x = position.x - layout.margin;
      links.setAttribute('position', position);
    }
  }
});
```

<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening

---
<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 4: Let's make it smooth

<ul>
  <li> Create a plane </li>
  <li> Add some buttons </li>
  <li> Try and do some layout </li>
</ul>

---
## Step 4: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```javascript
AFRAME.registerComponent('scrollleft', {
  schema: {
    on: { type: 'string' }
  },
  init: function()  {
    this.el.addEventListener(this.data.on, this.scroll);
  },
  scroll: function()
  {
    var data = this.data;

    //The current position is what we're modifying
    var links = document.querySelector("#links");
    var layout = links.getAttribute('layout');
    var position = links.getAttribute('position');
    var maxLeft =  -(layout.margin * layout.columns);
    if(position.x != maxLeft) {
      var newX = position.x - layout.margin;
      links.setAttribute('animation', 'from', position.x + ' ' + position.y + ' ' + position.z);
      links.setAttribute('animation', 'to', newX + ' ' + position.y + ' ' + position.z);
      links.emit('scrollpane');
      position.x = newX;
      links.setAttribute('position', position);
    }
  }
});


```
<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening

---
<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 5: Let's do some title text

<ul>
  <li> Create a plane </li>
  <li> Add some buttons </li>
  <li> Try and do some layout </li>
</ul>

---
## Step 5: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```html
        <!-- Image link template to be reused. -->
        <script id="link" type="text/html">
          <a-entity class="link"
            geometry="primitive: plane; height: 1; width: 1"
            material="shader: flat; src: ${thumb}"
            event-set__1="_event: mousedown; scale: 1 1 1"
            event-set__2="_event: mouseup; scale: 1.2 1.2 1"
            event-set__3="_event: mouseenter; scale: 1.2 1.2 1"
            event-set__4="_event: mouseleave; scale: 1 1 1"
            set-image="on: click; target: #image-360; title: #visible_title; value: ${title}; src: ${src}"
            sound="on: click; src: #click-sound"></a-entity>
        </script>
```

<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening

---
## Step 5: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```html
  <a-entity id="visible_title" position="0 -0.6 0.2" scale="4.0 4.0 4.0" text="color: white; align: center; value: This area intentionally blank"></a-entity>
```

<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening

---
## Step 5: Contined

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```javascript
AFRAME.registerComponent('set-image', {
  schema: {
    on: {type: 'string'},
    title: {type: 'selector'},
    value: {type: 'string'},
    target: {type: 'selector'},
    src: {type: 'string'},
    dur: {type: 'number', default: 300}
  },


```

<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening

---
## Step 5: Last Code Slide: PROMISE

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```javascript
  init: function () {
    var data = this.data;
    var el = this.el;

    this.setupFadeAnimation();

    el.addEventListener(data.on, function () {
      // Fade out image.
      data.target.emit('set-image-fade');
      // Wait for fade to complete.
      setTimeout(function () {
        // Set image.
        data.target.setAttribute('material', 'src', data.src);
        // Set text
        data.title.setAttribute('text','value', data.value);
      }, data.dur);
      //Set text
    });
  },

```

<!-- .element: class="stretch" -->

<!-- NOTES -->
- Get some UI awesomness happening


---
<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

# Step 6: CORDOVA

<ul>
  <li> Create a plane </li>
  <li> Add some buttons </li>
  <li> Try and do some layout </li>
</ul>

---
## Step 6: CORDOVA

<!-- .slide: data-background="media/img/aframe.jpg" data-transition="slide-in none" -->

```
cordova create WebVRDemo
cordova platform add ios/android
```
<!-- .element: class="stretch" -->

<!-- NOTES -->
- Create a Cordova App
- Make sure to bundle assets or use Whitelist
- CSP does NOT work with A Frame and Three.js (Seriously, it freaks out)

---

<!-- .slide: data-background="media/img/aframe.jpg" -->

## Works With Everything

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/d3.png">
    <i>d3.js</i>
  </div>
  <div>
    <img data-src="media/img/vue.png">
    <i>Vue.js</i>
  </div>
  <div>
    <img data-src="media/img/react.png">
    <i>React</i>
  </div>
  <div>
    <img data-src="media/img/redux.png">
    <i>Redux</i>
  </div>
  <div>
    <img data-src="media/img/jquery.png">
    <i>jQuery</i>
  </div>
  <div>
    <img data-src="media/img/angular.png">
    <i>Angular</i>
  </div>
</div>

<!-- NOTES -->

- Based on HTML, compatible with all existing libraries/frameworks
- Good reason to have HTML as an intermediary layer between WebGL/three.js
- All tools were on top of the notion of HTML
- Under the hood, A-Frame is an extensible, declarative framework for three.js...

------

# Entity-Component-System

<!-- .slide: data-background="media/img/standard-components.png" data-background-size="contain" -->

<!-- NOTES -->
- These are some components that ship with A-Frame
- A-Frame is fully extensible at its core so...

---

<!-- .slide: data-background="media/img/community-components.png" data-background-size="contain" -->

<!-- NOTES -->
- Community has filled the ecosystem with tons of components
- Components can do whatever they want, have full access to three.js and Web APIs
- The component ecosystem the lifeblood of A-Frame
- Physics, leap motion, particle systems, audio visualizations, oceans
- Drop these components as script tags and use them straight from HTML
- Advanced developers empowering other developers
- Working on collecting these components...

---

# Registry

<!-- .slide: data-background-color="#333" -->

Curated collection of A-Frame components.

<a class="stretch" href="https://aframe.io/aframe-registry">
  <video loop data-src="media/video/registrypreview.mp4" data-autoplay></video>
</a>

<!-- NOTES -->
- Collecting them into the A-Frame registry
- Like a store of components that we make sure work well
- People can browse and search for components or install them....

---

# Registry

<!-- .slide: data-background-color="#333" -->

Curated collection of A-Frame components.

<video loop data-src="media/video/leaphands.mp4" data-autoplay></video>


------

<!-- .slide: data-background="media/img/header.png" -->

# Community

https://aframe.io/blog/

---

<!-- .slide: data-background="media/img/apainter.gif" -->

# Art - *A-Painter*

@mozillavr

---

<!-- .slide: data-background="media/img/syria.gif" -->

# Journalism - *Fear of the Sky*

Amnesty International UK

---

<!-- .slide: data-background="media/img/mars.jpg" -->

# Journalism - *Journey to Mars*

The Washington Post

---

<!-- .slide: data-background="media/img/citybuilder.gif" -->

# Sandbox - *City Builder*

@kfarr

---

<!-- .slide: data-background="media/img/adit.gif" -->

# Data Visualization - *Adit*

@datatitian

---

<!-- .slide: data-background="media/img/a-blast.gif" -->

# Gaming - *A-Blast*

@mozillavr

---

<!-- .slide: data-background="media/img/ux.gif" -->

# Prototyping - *UI Widgets*

@whoyee

---

<!-- .slide: data-background="media/img/math.gif" -->

# Mathematics - *MathworldVR*

@sleighdogs

---

<!-- .slide: data-background="media/img/ar.gif" -->

# AR - *AR.js + A-Frame*

@jerome_etienne

---

<!-- .slide: data-background="media/img/webvrstudio.png" -->

# Tools - *WebVR Studio*

@webvrstudio

---

<!-- .slide: data-background-video="media/video/livetour.mp4" data-background-video-loop="true" -->

# Real Estate - *Live Tour*

iStaging

---

<!-- .slide: data-background="media/img/cadavr.gif" -->

# Education - *CadaVR*

@drryanjames

---

# aframe.io

<div class="captioned-image-row">
  <div>
    <img data-src="media/img/github.png">
    <i>125 contributors 5000 Stargazers</i>
  </div>
  <div>
    <img data-src="media/img/slack.png">
    <i>3000 members on Slack</i>
  </div>
  <div>
    <img data-src="media/img/scene-collage-circle.png">
    <i>100s of featured projects</i>
  </div>
</div>

<!-- NOTES -->
- Open source and inclusive project
- Most work done on GitHub
- Active community on Slack to share projects, interact, hang out, seek help
- Featured projects on the `awesome-aframe` repository and *A Week of A-Frame* blog
