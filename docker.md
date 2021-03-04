# Docker Intro

We are utilizing docker on our senior project for deployment and some utility tasks. The screenshot below shows an example of a docker image I created for our project which contains a collection
of protobuf and gRPC compilers for every language, and does the code generation for us. This is very useful as collecting the protobuf and gRPC compilers for all
languages is tedious, and code generation can be a hassle. Our image has all these items prepackaged so all a developer needs to do is run the image and mount the
proper directories, and all the code appears. You can see a usage below.

![docker](docker.png)

# Docker vs Host OS

Docker essentially is virtualizing the operating system for application running in the container. It achieves its great performance by using the operating system it is running, unlike a virtual machine which stands above the OS and tries to virtualize the hardware itself. Docker allows containers to run as though they are processes running on the host operating system, but are much more portable as their exact environment is defined in the image itself, making it perfectly reproducable. System calls can be handled by the host OS as intended, and thus system resources can be shared amongst containers. The modularity of individual containers is maintained by the fact that they have only read only access to the host OS services, and such cannot change anything without a bit of effort.
