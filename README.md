3DMNIST
=======

A 3D version of the [MNIST database of handwritten digits](http://yann.lecun.com/exdb/mnist/)

![3D MNIST](data/3Dmnist.png)

# CONTENT

The dataset includes 5000(train), 1000(valid) and 1000(test) [3D point clouds](https://en.wikipedia.org/wiki/Point_cloud) stored in [HDF5 file format](https://support.hdfgroup.org/HDF5/whatishdf5.html).

The files can be found in the `data` subfolder, containing 5000(train_small), 1000(valid_small) and 1000(test_small) [HDF5 groups](https://support.hdfgroup.org/HDF5/Tutor/fileorg.html)

Each group is named as its corresponding array index in the original mnist dataset (also included in the `data` subfolder) and it contains:

- "points" dataset: `x, y, z` coordinates of each 3D point in the point cloud.
- "normals" dataset: `nx, ny, nz` components of the unit normal associate to each point.
- "img" dataset: the original mnist image.
- "label" attribute: the original mnist label.

In the [3DMNIST notebook](http://nbviewer.jupyter.org/github/daavoo/3DMNIST/blob/master/3DMNIST.ipynb) you can find the code used to generate the dataset.

You can use the code in the notebook to generate a bigger 3D dataset from the original.

# CONTRIBUTIONS

In the `contrib` subfolder you can find examples on how to read/write the HDF5 files in Python and on how to generate global/local features to train predictive models.

New contributions are welcome via [pull_request](https://help.github.com/articles/about-pull-requests/). Please try to follow the schema of existing contributions.

Current contributions:
- voxelgrid: An example on how to generate a grid of voxels to extract a global feature vector and use that vector for training a linear model.
