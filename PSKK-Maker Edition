<html>
    <head>
    <script src="https://aframe.io/releases/0.9.2/aframe.min.js"></script>
    <script src="https://raw.githack.com/jeromeetienne/AR.js/master/aframe/build/aframe-ar.min.js"></script>
    <script src="https://raw.githack.com/donmccurdy/aframe-extras/master/dist/aframe-extras.loaders.min.js"></script>
    <script>
        AFRAME.registerComponent('loader', {
       init: function() {
         let loader = document.querySelector("#loadingEl")
         this.el.addEventListener('model-loaded', e => {
           console.log('loaded')
           loader.setAttribute("visible", "false")
         })
       }
     })
        
      </script>
       </head>
       
   <body>
      <a-scene vr-mode-ui="enabled: false" artoolkit='sourceType: webcam; detectionMode: mono; maxDetectionRate: 90;' arjs='debugUIEnabled: false;detectionMode: mono_and_matrix; matrixCodeType: 3x3;'>
         <!--  ALL  ASSETS  -->
         <a-assets>
         
    <!--   3D MODEL -->
            <a-entity  id="model" src=" INSERT URL SOURCE MODEL 3D HERE  " crossorigin="anonymous" rotation="-90 0 -90" position="0 0 0">
            </a-entity>
        
         </a-assets>
         
         <!--  ALL  ASSETS  -->
         <a-marker type="pattern" preset="pattern" url=" INSERT URL FOR MARKER PATTERN HERE  ">
           <a-box id="loadingEl"></a-box>
           <a-entity loader> 
          
            <a-entity position="0 0 0" gltf-model="#model"  material='transparent:true;shader:flat;side:double;metelness:2' rotation="0 0 0" scale="0.25 0.25 0.25"  shadow="receive: false"  >
            
            </a-entity>
           </a-entity>
         </a-marker>
         <a-entity camera>
            <a-entity cursor="rayOrigin: mouse;fuse: false;"></a-entity>
         </a-entity>
      </a-scene>
   </body>
</html>
