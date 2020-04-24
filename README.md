# Subutai-s3fs Blueprint 

**Subutai-s3fs Blueprint** allows create N containers in M peers. Containers will have a directory which is sync with your Minio bucket.

## Recruitments:

1) Make sure that container supports `fuse`

2) Install [Minio](https://bazaar.subutai.io/products/1437)


## Performance testing of similar software:

Similar softwar to test and compare are: **s3fs-fuse** , **goofys**, **riofs**

As testing tool selected **pngquant**.

**pngquant** is a command-line utility and a library for lossy compression of PNG images. It is ideal to test read and write speed for directory.

### Testing 
Minio cluster installed in 2 EU peers, cluster has 4 containers with 1 node in each. 40 png images uploaded initially.

Command to run test:

```shell
pngquant *.png
```

Time which took each softwere

```
s3fs-fuse - 80 seconds
goofys    - 17 seconds
riofs     - 32 seconds
```

Each software had similar environment setup.
