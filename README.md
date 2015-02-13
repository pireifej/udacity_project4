To run project 4, simplye visit the index.html of the root directory. The pizza web page can be found in the bottom-most hyperlink (accompanied by the Pokeball picture). Or just visit the public URL "http://pireifej.github.io/udacity_project4/". The optimizations can be found in comments by searching for "OPTIMIZATION" in main.js, but I listed them here for convenience:

Change pizza sizes
---

- Hard-coded the pizza sizes. I found that the calculations aren't necessary since you get the same size every time. I logged the calculated sizes and then hard coded them in the "sizes" object literal (292.5px for small, 389.961px for medium and 585px for large).
- We do not necessarily need to access the DOM object for every iteration whenever we use document.querySelectorAll(). Everytime we access the DOM, it takes a lot of time. So I access the DOM only once outside of the loop.

Scrolling
---
- Reduced the number of elements created for the sliding pizzas in the background. Instead of iterating 200 times and creating 200 different elements, I iterate 15 times instead. This improves the fps and the effect is the same (as well as number of pizzas!).
- Access the movingPizzas1 container and .mover items only once outside of the loop. Also, calculate the scrollTop only once outside of the loop.
- Compressed pizza.png to pizza_compressed.png. Reduced the size by 60% (30 KB total) via tinypng.com.