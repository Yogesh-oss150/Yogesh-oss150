.glitch {
  font-family: 'SFMono-Regular', Consolas, monospace;
  color: #00ff66;
  position: relative;
  display: inline-block;
  font-weight: bold;
}

.glitch::before,
.glitch::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.glitch::before {
  left: 2px;
  text-shadow: -2px 0 #ff0055;
  clip: rect(44px, 450px, 56px, 0);
  animation: glitch-anim 5s infinite linear alternate-reverse;
}

.glitch::after {
  left: -2px;
  text-shadow: -2px 0 #00ffff, 0 2px #ff0055;
  clip: rect(85px, 450px, 140px, 0);
  animation: glitch-anim2 5s infinite linear alternate-reverse;
}

@keyframes glitch-anim {
  0% { clip: rect(31px, 9999px, 94px, 0); }
  20% { clip: rect(11px, 9999px, 39px, 0); }
  40% { clip: rect(82px, 9999px, 12px, 0); }
  60% { clip: rect(51px, 9999px, 78px, 0); }
  80% { clip: rect(2px, 9999px, 63px, 0); }
  100% { clip: rect(44px, 9999px, 99px, 0); }
}

@keyframes glitch-anim2 {
  0% { clip: rect(76px, 9999px, 10px, 0); }
  20% { clip: rect(23px, 9999px, 89px, 0); }
  40% { clip: rect(90px, 9999px, 45px, 0); }
  60% { clip: rect(12px, 9999px, 67px, 0); }
  80% { clip: rect(55px, 9999px, 21px, 0); }
  100% { clip: rect(38px, 9999px, 74px, 0); }
}
