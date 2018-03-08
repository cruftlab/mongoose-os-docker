# Mongoose OS
This Docker image contains the [mos](https://mongoose-os.com/software.html)
tool installed, which can be used to build Mongoose OS firmware.

Please refer to the [Mongoose OS](https://mongoose-os.com/) official website for
more information.

# Usage
This image has the `mos` tool as its entrypoint, meaning you can think of it as
a Docker "extension" of the `mos` tool. Every argument you add to this container
will be used as an argument to the `mos` tool.

For example, to show the help menu (`mos --help`), run the following command:
```bash
docker run --rm -it cruftlab/mongoose-os --help
```

## Source files
In order to build the Mongoose OS firmware, you will need to mount the source files.
They are located under the `/sources/` volume.

For instance, if you want to initialize firmware source code in the `firmware` folder
inside your current folder, run the following command:

```bash
docker run --rm -it -v $PWD/firmware:/sources cruftlab/mongoose-os init
```

# Contribute
You're very welcome to solve (or report) an issue [here](https://github.com/cruftlab/mongoose-os-docker/issues)!

# Get started with Mongoose OS
There's a lot of good information on the [Mongoose OS](https://mongoose-os.com/)
official website. The [Mongoose OS book](https://mongoose-os.com/docs/book/intro.html)
should be a good starting point.

Happy coding!
