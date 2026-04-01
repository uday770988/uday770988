<div align="center">

  <!-- Simple Left-to-Right Tile Flip Banner -->
  <div style="width: 100%; max-width: 720px; height: 160px; perspective: 1200px; margin: 30px 0;">
    <div id="flipContainer" style="position: relative; width: 100%; height: 100%; transition: transform 1.2s ease-in-out; transform-style: preserve-3d; border-radius: 16px; box-shadow: 0 8px 25px rgba(0,0,0,0.15);">
      
      <!-- Front Side - Blue -->
      <div style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; background: linear-gradient(135deg, #0A66C2, #1E88E5); color: white; border-radius: 16px; display: flex; align-items: center; justify-content: center; font-size: 34px; font-weight: 700;">
        Uday Ahire
      </div>
      
      <!-- Back Side - Yellow -->
      <div style="position: absolute; width: 100%; height: 100%; backface-visibility: hidden; background: linear-gradient(135deg, #FFD700, #FFAA00); color: #1a1a1a; border-radius: 16px; display: flex; align-items: center; justify-content: center; font-size: 34px; font-weight: 700; transform: rotateY(180deg);">
        Data Science
      </div>
    </div>
  </div>

  <h1>Hi, I'm Uday Ahire 👋</h1>

  <p>
    <strong>B.Tech Computer Science & Engineering (6th Semester)</strong><br>
    Government College of Engineering, Nagpur
  </p>

  <p>
    Passionate about <strong>Machine Learning</strong> and <strong>Data Science</strong>.<br>
    Building practical AI solutions and turning data into meaningful impact.
  </p>

</div>

<style>
/* Auto left-to-right flip every 8 seconds */
#flipContainer {
  animation: horizontalFlip 8s infinite ease-in-out;
}

@keyframes horizontalFlip {
  0%    { transform: rotateY(0deg); }
  45%   { transform: rotateY(0deg); }
  55%   { transform: rotateY(180deg); }
  95%   { transform: rotateY(180deg); }
  100%  { transform: rotateY(0deg); }
}
</style>

---

### 🛠️ Technical Skills

- **Languages**: Python, Java, JavaScript, HTML, CSS, React
- **ML & Data Science**: NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn, TensorFlow, NLTK
- **Tools**: Git, Jupyter Notebook

---

### 🔥 Featured Projects

**Image Steganography Tool**  
Python-based application to hide secret text messages inside images using Least Significant Bit (LSB) technique.

- **Tech Stack**: Python, Pillow (PIL), Tkinter, NumPy
- [View Repository](https://github.com/yourusername/image-steganography)

*(Replace `yourusername` with your actual GitHub username and add your other projects)*

---

<div align="center">
Made with ❤️ in Nagpur
</div>
