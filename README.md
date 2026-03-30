<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ML → Data Science Horizontal Tile Animation</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@900&amp;display=swap');

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            background: #0f172a;
            font-family: 'Inter', system-ui, sans-serif;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            padding: 40px 20px;
            gap: 40px;
        }

        .header {
            text-align: center;
            color: white;
        }

        .header h1 {
            font-size: 2.8rem;
            font-weight: 900;
            background: linear-gradient(90deg, #ff8c00, #ffcc00);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 8px;
        }

        .header p {
            font-size: 1.1rem;
            opacity: 0.8;
        }

        .tile-container {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 6px;
            padding: 30px 40px;
            background: #1e2937;
            border-radius: 20px;
            box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.4);
            max-width: 100%;
            overflow-x: auto;
        }

        .tile {
            perspective: 1400px;
            width: 158px;
            height: 108px;
            flex-shrink: 0;
        }

        .tile-inner {
            position: relative;
            width: 100%;
            height: 100%;
            transform-style: preserve-3d;
            animation: flipTile 4800ms infinite linear;
            border-radius: 12px;
            box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.3),
                        inset 0 2px 0 rgba(255,255,255,0.2);
        }

        /* Staggered delays – creates left-to-right wave effect */
        .tile:nth-child(1) .tile-inner { animation-delay: 0ms; }
        .tile:nth-child(2) .tile-inner { animation-delay: -150ms; }
        .tile:nth-child(3) .tile-inner { animation-delay: -300ms; }
        .tile:nth-child(4) .tile-inner { animation-delay: -450ms; }
        .tile:nth-child(5) .tile-inner { animation-delay: -600ms; }
        .tile:nth-child(6) .tile-inner { animation-delay: -750ms; }
        .tile:nth-child(7) .tile-inner { animation-delay: -900ms; }
        .tile:nth-child(8) .tile-inner { animation-delay: -1050ms; }

        @keyframes flipTile {
            0%   { transform: rotateY(0deg); }
            18%  { transform: rotateY(180deg); }   /* fast flip to back */
            62%  { transform: rotateY(180deg); }   /* stay on DATA SCIENCE */
            80%  { transform: rotateY(360deg); }   /* fast flip back */
            100% { transform: rotateY(360deg); }   /* stay on ML */
        }

        .front, .back {
            position: absolute;
            width: 100%;
            height: 100%;
            display: flex;
            align-items: center;
            justify-content: center;
            backface-visibility: hidden;
            border-radius: 12px;
            overflow: hidden;
        }

        .front {
            background: linear-gradient(135deg, #ff8c00, #ff6200);
            color: white;
        }

        .back {
            background: linear-gradient(135deg, #ffcc00, #facc15);
            color: #1e2937;
            transform: rotateY(180deg);
        }

        .front-text {
            font-size: 54px;
            font-weight: 900;
            letter-spacing: -2px;
            text-shadow: 0 4px 8px rgba(0,0,0,0.3);
        }

        .back-text {
            font-size: 19px;
            font-weight: 900;
            letter-spacing: -0.5px;
            text-align: center;
            line-height: 1.1;
            text-shadow: 0 3px 6px rgba(0,0,0,0.2);
        }

        .tile::after {
            content: '';
            position: absolute;
            inset: 0;
            background: linear-gradient(
                90deg,
                rgba(255,255,255,0.15) 0%,
                rgba(255,255,255,0) 50%,
                rgba(255,255,255,0.15) 100%
            );
            pointer-events: none;
            border-radius: 12px;
            z-index: 2;
            opacity: 0.25;
        }

        /* README-friendly label */
        .readme-label {
            position: absolute;
            top: 12px;
            left: 12px;
            background: rgba(255,255,255,0.9);
            color: #1e2937;
            font-size: 10px;
            font-weight: 700;
            padding: 2px 8px;
            border-radius: 9999px;
            letter-spacing: 0.5px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.2);
        }

        .info {
            color: #64748b;
            font-size: 1rem;
            max-width: 620px;
            text-align: center;
            line-height: 1.5;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>ML → DATA SCIENCE</h1>
        <p>Horizontal Tile Flip Animation for GitHub README</p>
    </div>

    <div class="tile-container">
        <!-- Tile 1 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 2 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 3 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 4 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 5 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 6 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 7 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>

        <!-- Tile 8 -->
        <div class="tile">
            <div class="tile-inner">
                <div class="front">
                    <div class="front-text">ML</div>
                </div>
                <div class="back">
                    <div class="back-text">DATA<br>SCIENCE</div>
                </div>
            </div>
        </div>
    </div>

    <div class="info">
        ✅ Tiles start with <strong>ML</strong> (white on orange)<br>
        ✅ Tiles flip sequentially from left to right into <strong>DATA SCIENCE</strong> (black on yellow)<br>
        ✅ Full loop every ~4.8 seconds • Pure CSS • Works directly in GitHub README.md
    </div>

    <div style="margin-top: 20px; font-size: 0.9rem; opacity: 0.6;">
        Copy everything below this line into your <strong>README.md</strong> ↓
    </div>

    <pre style="background:#1e2937;color:#e2e8f0;padding:20px;border-radius:12px;max-width:820px;overflow-x:auto;font-size:13px;line-height:1.4;"><code>&lt;style&gt;
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@900&amp;display=swap');
.tile-container{display:flex;justify-content:center;gap:6px;padding:30px 40px;background:#1e2937;border-radius:20px;box-shadow:0 25px 50px -12px rgb(0 0 0 / 0.4)}
.tile{perspective:1400px;width:158px;height:108px;flex-shrink:0}
.tile-inner{position:relative;width:100%;height:100%;transform-style:preserve-3d;animation:flipTile 4800ms infinite linear;border-radius:12px;box-shadow:0 10px 15px -3px rgb(0 0 0 / 0.3),inset 0 2px 0 rgba(255,255,255,0.2)}
.tile:nth-child(1) .tile-inner{animation-delay:0ms}
.tile:nth-child(2) .tile-inner{animation-delay:-150ms}
.tile:nth-child(3) .tile-inner{animation-delay:-300ms}
.tile:nth-child(4) .tile-inner{animation-delay:-450ms}
.tile:nth-child(5) .tile-inner{animation-delay:-600ms}
.tile:nth-child(6) .tile-inner{animation-delay:-750ms}
.tile:nth-child(7) .tile-inner{animation-delay:-900ms}
.tile:nth-child(8) .tile-inner{animation-delay:-1050ms}
@keyframes flipTile{0%{transform:rotateY(0deg)}18%{transform:rotateY(180deg)}62%{transform:rotateY(180deg)}80%{transform:rotateY(360deg)}100%{transform:rotateY(360deg)}}
.front,.back{position:absolute;width:100%;height:100%;display:flex;align-items:center;justify-content:center;backface-visibility:hidden;border-radius:12px}
.front{background:linear-gradient(135deg,#ff8c00,#ff6200);color:white}
.back{background:linear-gradient(135deg,#ffcc00,#facc15);color:#1e2937;transform:rotateY(180deg)}
.front-text{font-size:54px;font-weight:900;letter-spacing:-2px;text-shadow:0 4px 8px rgba(0,0,0,0.3)}
.back-text{font-size:19px;font-weight:900;letter-spacing:-0.5px;text-align:center;line-height:1.1;text-shadow:0 3px 6px rgba(0,0,0,0.2)}
&lt;/style&gt;

&lt;!-- PASTE THIS HTML ANYWHERE IN YOUR README.md --&gt;
&lt;div class="tile-container"&gt;
  &lt;!-- 8 identical tiles --&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
  &lt;div class="tile"&gt;&lt;div class="tile-inner"&gt;&lt;div class="front"&gt;&lt;div class="front-text"&gt;ML&lt;/div&gt;&lt;/div&gt;&lt;div class="back"&gt;&lt;div class="back-text"&gt;DATA&lt;br&gt;SCIENCE&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;&lt;/div&gt;
&lt;/div&gt;</code></pre>

</body>
</html>
