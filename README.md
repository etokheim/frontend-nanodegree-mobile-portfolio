# Portfolio page - Performance improvements
This repository is my solution to a project from Udacity's frontend developer nanodegree program where the goal was to improve the sites performance.

For the blog, which is linked to below, I've improved the loading time considerably. You can see the difference by using Google's page speed test [here](https://developers.google.com/speed/pagespeed/insights/).
![A picture of my page speed test](https://raw.githubusercontent.com/etokheim/frontend-nanodegree-mobile-portfolio/master/website%20optimization.jpg)

The blog also includes a project called "Cam's Pizzeria" which had huge performance issues. On my computer the old version runs at about 20 fps, while the improved version easily hits 60 fps - even when I slow down my computer with Chrome's developer tools. If you check out the pizzeria page, I urge you to slow down your computer in order get a better idea of how much the page actually improved. To do this in Chrome, go to: developer tools --> timeline --> CPU throttle --> "Low end device (x5 slowdown)".

For a live demo you can go to:
 * [Improved version](https://etokheim.github.io/Udacity/08%20Website%20Optimization/frontend-nanodegree-mobile-portfolio/improved/)
 * [Original version](https://etokheim.github.io/Udacity/08%20Website%20Optimization/frontend-nanodegree-mobile-portfolio/original/)


## Download
When downloading you should append the --recursive command to ```$ clone [url] ``` in order to include the required submodule.
```bash
$ git clone --recursive https://github.com/etokheim/Udacity.git
```

Optionally, or if you didn't read the README file before cloning, you could do:
```bash
$ # If you've already cloned the repository, skip this step
$ git clone https://github.com/etokheim/Udacity.git

$ # Initializes the local .gitmodules
$ git submodule init

$ # Updates/downloads all submodules
$ git submodule update
```

## My improvements

### Portfolio
* Added HTML meta tag for caching.
* Inlined critical CSS resources.
* Delayed loading of non-critical CSS resources.
* Compressed pizzeria.jpg.
* Added media="print" attribute to print.css.
* Moved analytics scripts to separate file in order load it asynchronously.
	* Added defer attribute in order to delay execution till the page is finished parsing.

#### Further improvement suggestions:
* Use a web worker to move the moving pizzas.
* Use a web worker to resize pizzas when moving the slider.

### Pizzeria
* Removed FSL (Forced Synchronous Layout) event from changePizzaSizes() and wrapped the visual changes in requestAnimationFrame.
* Removed FSL in updatePositions() (function for moving pizzas in the background) and wrapped the visual changes in requestAnimationFrame.
* Added will-change: transform attribute to the moving pizzas in order for them to render on a separate layer.
