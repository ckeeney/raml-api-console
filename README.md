# raml-api-console
Run https://github.com/mulesoft/api-console from a docker image

To get started, simply run the docker image making sure to provide port mappings
```
docker run -p 9000:9000 -p 35729:35729 ckeeney/raml-api-console
```
And then you can see the docs in your browser:


![Image](/doc/default_simple.png?raw=true)

By default, this image displays the [simple.raml](https://github.com/mulesoft/api-console/blob/master/dist/examples/simple.raml) documentation that comes bundled with [mulesoft/api-console](https://github.com/mulesoft/api-console)

To show your own documentation, simply mount a volume at `/apis` in the container:

```
docker run -p 9000:9000 -p 35729:35729 -v $(pwd)/raml:/apis ckeeney/raml-api-console
```

![Image](/doc/custom_docs.png?raw=true)
