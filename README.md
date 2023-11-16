<!DOCTYPE html>
<html>
<head>
  <style>
    .container {
      position: relative;
      width: 200px;
      height: 200px;
    }
    .sunflower {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 150px;
      height: 150px;
      background-color: yellow;
      border-radius: 50%;
      overflow: hidden;
    }
    .sunflower:before {
      content: "";
      position: absolute;
      top: -15px;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: yellow;
      border-radius: 50%;
      animation: bloom 3s ease-in-out infinite;
    }
    .sunflower .petal {
      position: absolute;
      width: 50px;
      height: 200px;
      background-color: #FFC107;
      border-radius: 50%;
    }
    .petal:nth-child(odd) {
      transform: rotate(45deg);
    }
    .petal:nth-child(even) {
      transform: rotate(90deg);
    }
    .petal:before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: #FFC107;
      border-radius: 50%;
    }
    @keyframes bloom {
      0% {
        transform: scale(0);
        opacity: 0;
      }
      50% {
        opacity: 1;
      }
      100% {
        transform: scale(1);
        opacity: 0;
      }
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="sunflower">
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
      <div class="petal"></div>
    </div>
  </div>
</body>
</html>
