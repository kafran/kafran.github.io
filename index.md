---
layout: about
---

The tail of the mobile software-smith. 

<canvas id="canvas" height="550"></canvas>
<script src="https://unpkg.com/rive-js"></script>
<script>
    new rive.Rive({
        src: 'https://kafran.net/assets/animations/smith.riv',
        canvas: document.getElementById('canvas'),
        autoplay: true
    });
</script>
