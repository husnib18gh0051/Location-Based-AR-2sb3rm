# Location-Based AR Musical Notation
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <title>Location-based AR Musical Notation</title>
    <script src="https://aframe.io/releases/1.0.4/aframe.min.js"></script>
    <script src="https://unpkg.com/aframe-look-at-component@0.8.0/dist/aframe-look-at-component.min.js"></script>
    <script src="https://raw.githack.com/AR-js-org/AR.js/master/aframe/build/aframe-ar-nft.js"></script>
  </head>

  <body style="margin: 0; overflow: hidden;">
    <a-scene
      embedded
      loading-screen="enabled: false;"
      arjs="sourceType: webcam; debugUIEnabled: false;"
    >
      <a-assets>
        <a-asset-item
          id="animated-asset"
          src="https://cdn.glitch.com/1077bf11-8765-491c-a102-a18f737ef706%2Fcompile_asset.mp4?v=1631530365908"
        ></a-asset-item>
        <video
          src="https://cdn.glitch.com/1077bf11-8765-491c-a102-a18f737ef706%2Fcompile_asset.mp4?v=1631530365908"
          preload="auto"
          id="vid"
          response-type="arraybuffer"
          loop
          crossorigin
          webkit-playsinline
          autoplay
          playsinline
        ></video>
      </a-assets>

      <a-video
        src="#vid"
        position="0 30 0"
        rotation="0 180 0"
        look-at="[gps-camera]"
        videohandler
        smooth="true"
        smoothCount="10"
        smoothTolerance="0.01"
        smoothThreshold="5"
        autoplay="false"
        scale="10 10 10"
        gps-entity-place="latitude: 2.9325415728372493; longitude: 101.75336355956453;"
      ></a-video>

      <a-camera
        gps-camera="simulateLatitude:2.9325415728372493;simulateLongitude:101.75336355956453"
        rotation-reader
      ></a-camera>
    </a-scene>
  </body>
</html>
