The original owner of the project is https://github.com/msameeruddin/image-app

# Image Processing [App](https://process-image-app.herokuapp.com/)

![image_app_pic](https://user-images.githubusercontent.com/63333753/110889696-a70a8080-8314-11eb-9687-001c6de33888.PNG)

This is a simple image processing app containing operations like - 

* Image Equalization
* Image Flipping
* Image Mirroring
* Image Binarization
* Image Inversion
* Image Solarization

and transformations like - 

* Image Erosion
* Image Dilation
* Image Opening
* Image Closing
* Image Morphological Gradient
* Boundary Extraction

### Features

* User can upload the image file directly from his/her local folder.
* Toggle switch for converting the image into grayscale.
* The required output will be displayed in the output (side) window.

For sure additional operations and transformation will be added. You can checkout the app [here](https://process-image-app.herokuapp.com/).

## Deploy on Nife.io

You can deploy this application on [Nife.io](https://nife.io) using either the Git repository or the CLI.[1] [2]

### Option 1: Deploy from the Git repository

Deploy the project directly from GitHub.

| Setting | Value |
| --- | --- |
| Source | Git Repository |
| Provider | GitHub |
| Branch | `main` |
| Internal Port | `8080` |
| External Port | `80` |
| Build Mode | Auto-Dockerize with runtime |

### Option 2: Deploy with `nifectl`

If you prefer the command line, use the following workflow.

```bash
nifectl auth login
nifectl init
nifectl deploy
```

For step-by-step instructions, see the [Nife.io Quick Deploy documentation](https://docs.nife.io/overview/quick-deploy) and the [nifectl quick start guide](https://docs.nife.io/Quick-Start/Nifectl).


## References

1. (https://nife.io)
2. (https://docs.nife.io/deploy/python)