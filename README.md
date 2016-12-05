# Udacity
This repository is my solution to a project from Udacity's frontend developer nanodegree program.

## Download
When downloading you should append the --recursive command to ```bash $ clone [url] ``` in order to include the required submodule.
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
- Added HTML meta tag for caching
- Inlined critical CSS resources
- Delayed loading of non-critical CSS resources
- Compressed pizzeria.jpg
- Added media="print" attribute to print.css
- Moved analytics scripts to separate file in order load it asynchronously
	..- Added defer attribute in order to delay execution till the page is finished parsing

### Pizzeria
- Removed FSL (Forced Synchronous Layout) event from changePizzaSizes()