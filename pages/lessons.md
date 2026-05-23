---
layout: default
title: lesson 0
permalink: /lessons/
---
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>✨ Project Sparkle ✨</title>
<link href="{{ '/assets/css/style.css' | relative_url }}" rel="stylesheet" />
</head>


<body class='cats'>


<header class="navbar">
  <nav id="nav-links" class="nav-links">
    <a href="/sparkle_workshop/">Home</a>
    <a href="/sparkle_workshop/about/">Instructor</a>
    <a href="/sparkle_workshop/lessons/">Lessons</a>
    <a href="/sparkle_workshop/workshop/">Workshop</a>
  </nav>
  <div class="hamburger" onclick="toggleMenu()">🍔</div>
</header>

<!-- Gif Container -->
<div class="gif-container">
  <img src="https://github.com/LilaShiba/flora_dress/raw/main/assets/videos/iterate.gif" alt="Iteration GIF" style="max-width: 75%; height: auto;">
</div>
  
  <section>
    <h2>🌟 What You Need 🌟</h2>
    <p>Before you start, make sure you have the following:</p>
    <ul>
      <li><strong>Microcontroller</strong> (e.g., the Flora itself) ⚡</li>
      <li><strong>Flora NeoPixel Strip</strong> (or a single Flora NeoPixel) 🌈</li>
      <li><strong>Jumper Wires</strong> 🔌</li>
    </ul>
  </section>

<div class="gif-container">
  <img src="https://raw.githubusercontent.com/LilaShiba/flora_dress/main/assets/videos/example.gif" alt="Iteration GIF" style="max-height: 500px; width: auto;">
</div>


  <section class="step">
    <details>
      <summary>⚙️ Step 1: Wiring the Flora NeoPixel ⚙️</summary>
      <p>Here’s how to wire up your <strong>Flora NeoPixel</strong>:</p>
      <ol>
        <li>
          <strong>Connect the Flora NeoPixel</strong> using jumper wires:
          <ul>
            <li><strong>Data Pin</strong>: Pin A1 on Flora</li>
            <li><strong>Power (VCC)</strong>: 5V</li>
            <li><strong>Ground (GND)</strong>: GND</li>
          </ul>
        </li>
        <li>Your setup should look like this:</li>
        <img src="https://cdn-learn.adafruit.com/assets/assets/000/069/730/large1024/led_pixels_cpx_alligatorclips.jpg?1548106119" 
             alt="Flora NeoPixel Wiring Diagram" 
             style="max-width: 100%; height: auto;" />
      </ol>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🔥 Step 2: Install the Adafruit NeoPixel Library 🌈</summary>
      <p>1. Open the <strong>Arduino IDE</strong>.</p>
      <p>2. Navigate to <strong>Sketch > Include Library > Manage Libraries</strong>.</p>
      <p>3. Search for "<strong>Adafruit NeoPixel</strong>" and click <strong>Install</strong>.</p>
      <p><a href="https://www.arduino.cc/en/software/" class="button">Get the IDE HERE</a></p>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>💡 Step 3: Load the Example Code ✨</summary>
      <p>We’ll use the <strong>strandtest</strong> example from the NeoPixel library:</p>
      <ol>
        <li>Open your <strong>Arduino IDE</strong>.</li>
        <li>Go to <strong>File > Examples > Adafruit NeoPixel > strandtest</strong>.</li>
      </ol>
      <pre><code>
#include &lt;Adafruit_NeoPixel.h&gt;

#define PIN        6
#define NUMPIXELS  16

Adafruit_NeoPixel strip(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);

    void setup() {
            strip.begin();
            strip.show();
          }

          void loop() {
            for (int i = 0; i &lt; strip.numPixels(); i++) {
              strip.setPixelColor(i, strip.Color(255, 0, 0)); // Red
              strip.show();
              delay(50);
      }
    }
      </code></pre>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🚀 Step 4: Upload & Run 🚀</summary>
      <p>1. Connect your Arduino via USB.</p>
      <p>2. Select your board and port in <strong>Tools</strong>.</p>
      <p>3. Click <strong>Upload</strong> and enjoy the lights! 🎇</p>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🎉 Congratulations! 🎉</summary>
      <p>You’ve successfully lit up your <strong>Flora NeoPixel</strong> strip! 🌈✨</p>
    </details>
  </section>

  <h2 class="shimmer-text">🦆 Rubber Ducky 🦆</h2>
  <p>A rubber ducky is a programmer's best friend for figuring out bugs. Explain your code line-by-line to a duck (or friend, cat, etc.) to spot mistakes.</p>

  <section class="step">
    <details>
      <summary>🌙 Debugging Alone 🌙</summary>
      <ul>
        <li>🔄 Change one thing at a time — and if it doesn’t work, change it back! Keep experiments small and reversible.</li>
        <li>📝 Take notes as you go — track what you tried so you don't go in circles!</li>
        <li>🎯 Try the easiest thing first — sometimes it's just a missing semicolon 😅.</li>
      </ul>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🤝 Debug with a Friend 🤝</summary>
      <ul>
        <li>🤝 Pair Programming — two minds are better than one! Even just talking through the problem together can spark ideas.</li>
        <li>🔍 Research like a pro — Google your error messages exactly, add the language/framework (e.g., "Python list index out of range"), and check sites like StackOverflow, GitHub Issues, or official docs first.</li>
      </ul>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🌈 Next Steps 🌙</summary>
      <ul>
        <li>Change color to <strong>green</strong>: <code>strip.Color(0, 255, 0)</code></li>
        <li>Try different animations to make it dance! 💃</li>
      </ul>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>🌟 Troubleshooting Tips 🌟</summary>
      <ul>
        <li><strong>No lights?</strong> Double-check your wiring.</li>
        <li><strong>Blurry color?</strong> Use a proper 5V power supply.</li>
      </ul>
    </details>
  </section>

  <h2 class="shimmer-text">Commands</h2>
  <p>Use these commands to change colors, brightness, and LED count:</p>

  <section class="step">
    <details>
      <summary>🔧 Changing the Color 🎨</summary>
      <p>Change RGB values with:</p>
      <pre><code>
strip.setPixelColor(pixel, strip.Color(red, green, blue));
      </code></pre>
      <p>Example for green:</p>
      <pre><code>
strip.setPixelColor(i, strip.Color(0, 255, 0));
      </code></pre>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>💡 Adjusting the Brightness</summary>
      <p>Use <code>strip.setBrightness(value)</code> (0–255):</p>
      <pre><code>
strip.setBrightness(128);  // 50% brightness
      </code></pre>
    </details>
  </section>

  <section class="step">
    <details>
      <summary>📏 Setting the Number of Pixels</summary>
      <p>Edit the <code>NUMPIXELS</code> value:</p>
      <pre><code>
#define NUMPIXELS 10
      </code></pre>
    </details>
  </section>


  <!-- JS at the end for better performance -->
<script src="{{ site.baseurl }}/assets/js/cats.js"></script>
<script src="{{ site.baseurl }}/assets/js/mouse.js"></script>
<script src="{{ site.baseurl }}/assets/js/confetti.js"></script>
<script src="{{ site.baseurl }}/assets/js/expandEffect.js"></script>

</body>
</html>
