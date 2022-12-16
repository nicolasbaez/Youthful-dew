# Youthful-dew
I need to study caligraphy

![buh](https://github.com/nicolasbaez/Abundant-patella/blob/main/ezgif-4-d922e3eb98.gif)
```javascript
x = [];
y = [];
z = [];
k = 0;
w = 500;
setup = (_) => {
  createCanvas(w, w);
  for (i = 1; i < w; i++) {
    x[i] = random(w);
    y[i] = random(w);
  }
};
draw = (_) => {
  background(255);
  noFill();
  strokeWeight(3);
  beginShape();
  for (i = 0; i <= map(cos(radians(k)), 1, -1, 0, w / 8); i++) {
    curveVertex(x[i], y[i]);
  }
  endShape();
  k++;
};
function keyPressed() {
  if (key === "s") {
    saveGif("xp001.gif", 360, { delay: 0, units: "frames" });
  }
}
