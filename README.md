# Isometric Tilemaps

### Steps I followed:

1. First, I imported the sprites and set their pivot points at the center of the ground. Also I set the sprites custom outlines to fit its pixels to avoid rendering transparencies and save resources.

![](https://i.gyazo.com/9a2e7bd7015e6177ddce4dda5534bf2a.png)

![](https://i.gyazo.com/9d068b25209d70ab9ac11863c394bce1.png)

2. Then, I created a GameObject 2D Isometric Grid Z as Y and adjusted its Cell Size (X and Y) to fit my sprite, in my case x:1.25 y:0.625. Also, I set z:1 to make it work in different Z heights. I set the same values to the Palette Prefab itself.

3. I set its Tilemap Renderer Mode to "Individual" instead of "Chunk", as the last one isn't support in scene view (touble is that it's less performant).

4. Finally, to make Z height work properly, I set "Transparency Sort Mode" to "Custom Axis" x:0, y:1, z:0.49, in Edit > Settings > Graphics.

![](https://i.gyazo.com/4f7e21da0193ab9d6a7b41e70fa690c7.png)

Now, to place a sprite in the scene use its Z position as its grounded height in the tilemap.

---

Next thing I wonder is how to implement physics and movement above the isometric plane properly.
