### Notice
I have forked [this repo](https://github.com/artificially-ai/kaggle_toxicity) to reupload the docker contains as the old ones were not available anymore.

# Kaggle - Toxicity Challenge

This repositoru aims to share some of the code I wrote for the [Toxicity Challenge](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge).
I did not make it to the first positions, but getting access to the dataset and being able to try it out on AWS GPU
instances was worth it.

The datasets, for both training and testing, are not available in this repository, but they can be easily download at
the Toxicity data page: [datasets](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge/data)

The model built here uses an activation function I have developed myself, which was part of the IBM Watson AI XPRIZE
competition. The function has demonstrated to be better than the ReLU function. More about the ReLUs function (as I call it),
will soon be available in a separate paper, as there is a hyper parameter that needs to be tuned depending on the network architecture.

## Performance

### MacBook Pro

On a MacBook Pro, with 16GB, 4 cores, Intel i7, one epoch takes about 30 minutes.

### AWS

On a g2.2xlarge GPU Instance, with 15GB and 8 vCPUs, one epoch takes about 3 minutes. Quite impressive!

# Running the Model

## Running with Docker

The Docker image, which contains the source code, is executed from another poject which is able to spin up a whole AWS environment for the model to run.
Since it depends on the NVIDIA Cuda Drivers, it won't be possible to run it locally.

More information on running it with Terraform can be found in the [Automated ML](https://github.com/ekholabs/automated_ml) repository.