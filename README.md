# CZB-zarr-challenge

1. **Clone or install** the package:
   ```bash
   git clone https://github.com/yourusername/czb-zarr-challenge.git
   cd czb-zarr-challenge
   pip install -e .

Or, install using PyPI:
`pip install czb-zarr-challenge`

## Data downloads
data folder should just be empty when first uploaded into the repo
KazanskyStar command:
20241107 command:

## iohub download
to get latest version (0.3.0):
`git clone https://github.com/czbiohub-sf/iohub.git`
`pip install ./iohub`

To convert OME-TIFF to OME-Zarr using iohub:
`python tiff_to_zar.py `
This uses TiffConverter from iohub's convert module, and by default is shown on Dataset 1 which is a Micromanager OME-TIFF dataset.

To generate a metadata .txt file with key metadata from a Zarr store, run:
czb-zarr-challenge metadata \
    --store /path/to/YourData.zarr \
    --out ./example_metadata.txt

For Dataset 1, run 
czb-zarr-challenge metadata -data/KazanskyStar_converted.zarr metadata1.txt
czb-zarr-challenge metadata -data/20241107_infection.zarr metadata2.txt

The functionality code is found in `get_metadata.py`. It uses iohub's open_ome_zarr function () and takes advantage of iohub's node objects to ____.

This will print the OME-Zarr hierarchy (trees and group names) to stdout, and will save a human-readable example_metadata.txt containing shape, chunk size, dtype, scale, and channel names.

## Inference Profiling

A custom PyTorch DataLoader that uses iohub and the OME-Zarr (Dataset 2) to
read data can be found in dataloader.py. We use this to profile the time it takes to read the data and to run inference with a pre-trained ResNet model.

Run the run_inference subcommand
czb-zarr-challenge run_inference data/20241107_infection.zarr

## Nuclei Segmentation







Task 1 deliverables:
()
()


API:

To segment ()
Run () from scripts/(). 
Output will be in outputs/().


CHECK THAT EACH SCRIPT AND EACH OUTPUT HAS BEEN COVERED HERE!