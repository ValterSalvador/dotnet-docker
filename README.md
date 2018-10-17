This repository contains `Dockerfile` definitions for Docker images that I use.

See [dotnet/dotnet-docker](https://hub.docker.com/r/microsoft/dotnet/) for images with official releases of [.NET Core](https://github.com/dotnet/core).

# Latest Version of Common Tags

The following tags are the latest stable versions of the most commonly used images. The complete set of tags is listed further down.

- [`2.1-sdk`](https://github.com/dotnet/dotnet-docker/blob/nightly/2.1/sdk/stretch/amd64/Dockerfile)
- [`2.1-aspnetcore-runtime`](https://github.com/dotnet/dotnet-docker/blob/nightly/2.1/aspnetcore-runtime/stretch-slim/amd64/Dockerfile)
- [`2.1-runtime`](https://github.com/dotnet/dotnet-docker/blob/nightly/2.1/runtime/stretch-slim/amd64/Dockerfile)

The [.NET Core Docker samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md) show various ways to use .NET Core and Docker together. See [Building Docker Images for .NET Core Applications](https://docs.microsoft.com/dotnet/core/docker/building-net-docker-images) to learn more.

Watch [dotnet/announcements](https://github.com/dotnet/announcements/labels/Docker) for Docker-related .NET announcements.

### Container sample: Run a simple application

Type the following command to run a sample console application:

```console
docker run --rm valtersalvador/dotnet-samples
```

### Container sample: Run a web application

Type the following command to run a sample web application:

```console
docker run -it --rm -p 5000:5000 --name dotnet_core_watcher valtersalvador/dotnet-watcher-samples:aspnetapp
```

After the application starts, navigate to `http://localhost:5000` in your web browser. On Windows, you may need to navigate to the container via IP address. See [ASP.NET Core apps in Windows Containers](https://github.com/dotnet/dotnet-docker/blob/master/samples/aspnetapp/aspnetcore-docker-windows.md) for instructions on determining the IP address, using the value of `--name` that you used in `docker run`.

See [Hosting ASP.NET Core Images with Docker over HTTPS](https://github.com/dotnet/dotnet-docker/blob/master/samples/aspnetapp/aspnetcore-docker-https.md) to use HTTPS with this image.

## Tags

# Linux amd64 tags

- [`2.1.402-sdk-watcher`, `sdk-watcher`, `watcher-latest` (*2.1/sdk/watcher/Dockerfile*)](https://github.com/ValterSalvador/dotnet-docker/blob/master/2.1/sdk/watcher/Dockerfile)

## Licenses

* [.NET Core license](https://github.com/dotnet/dotnet-docker/blob/master/LICENSE)
* [Windows Nano Server license](https://hub.docker.com/r/microsoft/nanoserver/) (only applies to Windows containers)
* [Pricing and licensing for Windows Server 2016](https://www.microsoft.com/en-us/cloud-platform/windows-server-pricing)

## Related Repos

.NET Core Docker Hub repos:

* [microsoft/aspnetcore](https://hub.docker.com/r/microsoft/aspnetcore/) for ASP.NET Core images.
* [microsoft/dotnet](https://hub.docker.com/r/microsoft/dotnet/) for .NET Core images.
* [microsoft/dotnet-samples](https://hub.docker.com/r/microsoft/dotnet-samples/) for .NET Core sample images.

.NET Framework Docker Hub repos:

* [microsoft/aspnet](https://hub.docker.com/r/microsoft/aspnet/) for ASP.NET Web Forms and MVC images.
* [microsoft/dotnet-framework](https://hub.docker.com/r/microsoft/dotnet-framework/) for .NET Framework images.
* [microsoft/dotnet-framework-samples](https://hub.docker.com/r/microsoft/dotnet-framework-samples/) for .NET Framework and ASP.NET sample images.
