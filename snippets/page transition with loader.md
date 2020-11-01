``` html
<div class="loader">
  <div class="bar1"></div>
  <div class="bar2"></div>
  <div class="bar3"></div>
  <div class="bar4"></div>
  <div class="bar5"></div>
  <div class="bar6"></div>
</div>
```

``` css
@-webkit-keyframes delay {
  0%,
  40%,
  100% {
    transform: scaleY(0.05);
    -webkit-transform: scaleY(0.05);
  }
  20% {
    transform: scaleY(1);
    -webkit-transform: scaleY(1);
  }
}
@keyframes delay {
  0%,
  40%,
  100% {
    transform: scaleY(0.05);
    -webkit-transform: scaleY(0.05);
  }
  20% {
    transform: scaleY(1);
    -webkit-transform: scaleY(1);
  }
}
body:before, body:after {
  content: "";
  height: 50vh;
  width: 100%;
  position: fixed;
  left: 0;
