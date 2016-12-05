# Udacity
My projects from Udacity's frontend nanodegree course. They are combined to avoid creating 20 separate repositories. Forked repositories are added as nested repositories (submodules).

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