---
layout: about
---

Hey there 👋🙂 

<canvas id="canvas" width="700" height="750"></canvas>
<script src="https://unpkg.com/rive-js"></script>
<script>
    new rive.Rive({
        src: 'https://kafran.net/assets/animations/smith.riv',
        canvas: document.getElementById('canvas'),
        autoplay: true
    });
</script>
