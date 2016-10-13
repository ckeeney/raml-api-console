# raml-api-console
Run https://github.com/mulesoft/api-console from a docker .

Check it out on [Dockerhub](https://hub.docker.com/r/ckeeney/raml-api-console/).

To get started, simply run the docker image making sure to provide port mappings
```
docker run -p 9000:9000 -p 35729:35729 ckeeney/raml-api-console
```
And then you can see the docs in your browser:


![Image](https://raw.githubusercontent.com/ckeeney/raml-api-console/master/doc/default_simple.png)

By default, this image displays the [simple.raml](https://github.com/mulesoft/api-console/blob/master/dist/examples/simple.raml) documentation that comes bundled with [mulesoft/api-console](https://github.com/mulesoft/api-console)

To show your own documentation, simply mount a volume at `/apis` in the container:

```
docker run -p 9000:9000 -p 35729:35729 -v $(pwd)/raml:/apis ckeeney/raml-api-console
```
Your main documentation must be available in the container at `/apis/main.raml`.

![Image](https://raw.githubusercontent.com/ckeeney/raml-api-console/master/doc/custom_docs.png)
