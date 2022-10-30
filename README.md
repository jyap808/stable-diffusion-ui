# Stable Diffusion UI

Fork of https://github.com/cmdr2/stable-diffusion-ui. Specifically the v1.22 tag.

## Background

This pulls down the Replicate Stable Diffusion set up.

Replicate uses their in-house Cog which exposes models to be run via a web URL call.

Docker packages up the model and the Cog interface.

Includes an addition web UI that can interface with Cog.

I've made design choices and changes based on person RTX 2080 graphics card.

## Changes

* Update to a newer Replicate model version
* UI cleanups and simplification
* Modify image_to_image.py
  * Remove NSFW check
* Modify predict.py
  * Remove NSFW check
  * Change some image dimension options

# System Requirements
1. Computer capable of running Stable Diffusion.
2. Linux.
3. Requires [Docker](https://docs.docker.com/engine/install/) and [nvidia-container-toolkit](https://stackoverflow.com/a/58432877).


# Installation
1. Clone this repository
2. Open your terminal, and in the project directory run: `docker compose up &` (warning: this will take some time during the first run, since it'll download Stable Diffusion's [docker image](https://replicate.com/stability-ai/stable-diffusion), nearly 17 GiB)
3. Open http://localhost:9000 in your browser. That's it!

To stop the server, please run `docker compose down`

# Usage

Open http://localhost:9000 in your browser (after running `docker compose up &` from step 2 previously).

# Disclaimer
The authors of this project are not responsible for any content generated using this interface.

This license of this software forbids you from sharing any content that violates any laws, produce any harm to a person, disseminate any personal information that would be meant for harm, spread misinformation and target vulnerable groups. For the full list of restrictions please read [the license](LICENSE).
