### HTML:
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

### CSS:
``` css
@-webkit-keyframes delay {
  0%, 40%, 100% {
    transform: scaleY(0.05);
    -webkit-transform: scaleY(0.05);
  }
  20% {
    transform: scaleY(1);
    -webkit-transform: scaleY(1);
  }
}
@keyframes delay {
  0%, 40%, 100% {
    transform: scaleY(0.05);
    -webkit-transform: scaleY(0.05);
  }
  20% {
    transform: scaleY(1);
    -webkit-transform: scaleY(1);
  }
}
body:before, body:after {
  content: '';
  height: 50vh;
  width: 100%;
  position: fixed;
  left: 0;
  background: #1c2020;
  z-index: 1;
  -webkit-transition: all .2s;
  transition: all .2s;
}
body:before {
  top: 0;
  -webkit-transform: translateY(-100%);
          transform: translateY(-100%);
}
body:after {
  bottom: 0;
  -webkit-transform: translateY(100%);
          transform: translateY(100%);
}
body.show:before {
  top: 50%;
}
body.show:after {
  bottom: 50%;
}
body.show .loader {
  opacity: 1;
  -webkit-transition: all .2s linear .2s;
  transition: all .2s linear .2s;
}

h1 {
  color: #1c2020;
  margin-bottom: 1em;
  font-size: 2.2rem;
  font-weight: 100;
}

.loader {
  margin: 0 auto;
  width: 60px;
  height: 50px;
  text-align: center;
  font-size: 10px;
  position: absolute;
  top: 50%;
  left: 50%;
  -webkit-transform: translateY(-50%) translateX(-50%);
          transform: translateY(-50%) translateX(-50%);
  z-index: 500;
  opacity: 0;
}
.loader > div {
  height: 100%;
  width: 8px;
  display: inline-block;
  float: left;
  margin-left: 2px;
  -webkit-animation: delay 0.8s infinite ease-in-out;
          animation: delay 0.8s infinite ease-in-out;
}
.loader .bar1 {
  background-color: #754fa0;
}
.loader .bar2 {
  background-color: #09b7bf;
  -webkit-animation-delay: -0.7s;
          animation-delay: -0.7s;
}
.loader .bar3 {
  background-color: #90d36b;
  -webkit-animation-delay: -0.6s;
          animation-delay: -0.6s;
}
.loader .bar4 {
  background-color: #f2d40d;
  -webkit-animation-delay: -0.5s;
          animation-delay: -0.5s;
}
.loader .bar5 {
  background-color: #fcb12b;
  -webkit-animation-delay: -0.4s;
          animation-delay: -0.4s;
}
.loader .bar6 {
  background-color: #ed1b72;
  -webkit-animation-delay: -0.3s;
          animation-delay: -0.3s;
}

main {
  height: 100vh;
  /* padding: 10px; */
  text-align: center;
}
```
### JS:
``` javascript
setInterval(transition, 4000);
setTimeout(function() {
   setInterval(stop, 4000);
 }, 2000);

function transition() {
  var body = document.querySelector('body');
  body.classList.add('show');
}

function stop() {
  var body = document.querySelector('body');
  body.classList.remove('show');
}
```
