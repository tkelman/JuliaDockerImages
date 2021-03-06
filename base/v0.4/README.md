## Julia 0.4 Docker Image

This docker image bundles: 
- Latest Julia 0.4.x
- IJulia

image: julialang/julia
version: 0.4.x (replace x with the latest minor version number)

## Getting the image:

To pull a pre-built image from dockerhub, run `docker pull <image>:<version>`

Alternatively, to build locally, run `git clone https://github.com/tanmaykm/JuliaDockerImages.git && docker build -t julialang/julia:v0.4.x JuliaDockerImages/base/v0.4`

## Running

- Run to get a shell prompt: docker run -it <image>:<version>
- Run Julia: docker run -it --entrypoint="/opt/julia/bin/julia" <image>:<version>
- Run IJulia: docker run -it --net="host" --entrypoint="/usr/local/bin/ipython" <image>:<version> notebook --profile julia
