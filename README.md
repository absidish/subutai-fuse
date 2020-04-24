# Subutai-s3fs Blueprint 

**Subutai-s3fs Blueprint** allows create N containers in M peers. Containers will have a directory which is sync with your Minio bucket.

## Recruitments:

1) Make sure that container supports `fuse`

2) Install [Minio](https://bazaar.subutai.io/products/1437)


## Performance testing of similar software:

**s3fs-fuse** 

**goofys**

**riofs**


**pngquant** is a command-line utility and a library for lossy compression of PNG images. It is ideal to test read and write speed for directory.

### Testing 
  Minio cluster has 40 png images.

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
