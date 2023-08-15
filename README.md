<!DOCTYPE html>
<html>
<head>
    <script src="https://aframe.io/releases/0.5.0/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-event-set-component@3.0.3/dist/aframe-event-set-component.min.js"></script>
</head>
<body>
    <!-- The main A-Frame scene -->
    <a-scene>
        <!-- GLTF model entity representing the chair -->
        <a-entity gltf-model="url(model.glb)"
                  radius="0.5" height="1.5"
                  position="0 1 -5"
                  event-set__enter="_event: mouseenter; _target: #model; visible: true"
                  event-set__leave="_event: mouseleave; _target: #model; visible: false">
            
            <!-- Text entity to display information about the chair -->
            <a-text id="model"
                    value="Product:  BAR chair
                    Type:   Fabric , Foam
                    Origin: Portugal
                    color:  Blue
                    Net Quantity:   1
                    W x H xD:   1050 mm x 400 mmx 400 mm
                    Weight: 10 kg
                    Price:  Rs 6,499
                    Description:    Elevate your dining or entertainment area with the perfect blend of style and sturdiness – the Fabric and Metal Bar Chair. This sleek and modern bar chair effortlessly combines the industrial appeal of metal with the comfort of fabric upholstery, creating a chic seating solution that enhances both aesthetics and functionality."
                    position="2.5 3 -5" scale="1.5 1.5 1" color="black"
                    geometry="primitive: plane; width: 1.75" material="color: #333"
                    visible="false">
            </a-text>
        
        </a-entity>
        
        <!-- Camera entity with cursor for interaction -->
        <a-camera>
            <a-cursor></a-cursor>
        </a-camera>
        
        <!-- Sky background color -->
        <a-sky color="#4CC3D9"></a-sky>
    </a-scene>
</body>
</html>
