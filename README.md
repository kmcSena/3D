# egvr.js

## sample

[DEMO](https://taisukef.github.io/vr-spiral/)
```html
<script type="module">
import * as eg from "https://js.sabae.cc/egvr.js";

for (let i = 0; i < 200; i++) {
  const th = i / 3;
  const r = 2 - i / 100 * 2;
  const x = Math.cos(th) * r;
  const y = Math.sin(th) * r;
  const s = r / 4;
  eg.sphere(x, i / 30, y, s, eg.rgb(i * 2, 0, 30));
}
</script>
```

[Interactive DEMO](https://code4fukui.github.io/egvr/interactive.html)
```html
<script type="module">
import * as eg from "https://js.sabae.cc/egvr.js";

;eg.box(0, .5, -5, 1, eg.hsl(180, 1, 0.5)).onclick = (e) => {
  e.target.setAttribute("visible", !e.target.getAttribute("visible"));
};

eg.model("https://code4fukui.github.io/vr-kanazawa-it/kanta.glb", 1, 0, -5).onclick = (e) => {
  e.target.setAttribute("position", { x: 1, y: 1, z: -5 });
  setTimeout(() => {
    e.target.setAttribute("position", { x: 1, y: 0, z: -5 });
  }, 1000);
};
</script>
```

[Game DEMO](https://code4fukui.github.io/egvr/game.html)

## slide

- [VR入門 PDF](https://code4fukui.github.io/egvr/VR-firststep.pdf)

## blog

- [QuestでもWebAR解禁! 福井県高校にてVR入門、体験/検索/発想/創造](https://fukuno.jig.jp/3792)
- [ディスプレイとして便利なARメガネ「Nreal Air」でキラキラな目を実現、高専JOINTフォーラムでも待望、スマートグラス](https://fukuno.jig.jp/3794)
