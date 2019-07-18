# How to Add Trianglify
- Go to the [trianglify github](https://github.com/qrohlf/trianglify)
- Add this `<script>` inside your `index.html` `<head>` somewhere above the `<script src="script.js"></script>` tag
      
      <script src="https://cdnjs.cloudflare.com/ajax/libs/trianglify/2.0.0/trianglify.min.js"></script>
- Inside your `script.js` add these lines

        var pattern = Trianglify({
          width: window.innerWidth,
          height: window.innerHeight
        });
        $("body").append(pattern.canvas())
        
- Inside your `style.css` add these lines:

        canvas {
          position: fixed;
          width: 100vw;
          height: 100vh;
          top: 0;
          left: 0;
          z-index: -1;
        }
        
        
 - Explore how to change the triangle size, variance, and colors here: http://qrohlf.com/trianglify/ . For example:
 
        var pattern = Trianglify({
          variance: "0.14",
          cell_size: 110, 
          seed: 'wrauj', 
          x_colors: 'Spectral',
          width: window.innerWidth,
          height: window.innerHeight,

        });
        $("body").append(pattern.canvas())
 
 
