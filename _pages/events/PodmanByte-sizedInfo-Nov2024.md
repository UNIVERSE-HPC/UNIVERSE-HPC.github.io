# Podman for the Byte-sized RSE Containers Session: Information and Installation Guidance

To support our byte-sized RSE containers session, we'll be using [**podman**](https://podman.io/).

### Podman Overview

podman is a fully-open source, lightweight container engine with an associated command line interface that is very similar to that provided by [Docker](https://www.docker.com/). Indeed, if you're attending this session because you're interested to work with Docker, all the commands we'll be showing you will operate with the same behaviour in Docker by simply replacing the `podman` with `docker`!

podman is "Linux native" which means that it needs to run in a Linux environment. However, solutions are provided to install and run podman on Linux, macOS and Windows. If you're just after information on how to install podman, you can jump to the [install information](#installing-podman) below.

_Note that Podman Desktop is a different tool to the podman container engine itself. When you install Podman Desktop, it also installs podman on your system, however, for the purpose of this session, we will use only the podman container engine and the command line interface (CLI) tool - you do not need to install Podman Desktop to participate in this session, only the underlying podman tool itself._

### Podman on macOS and Windows

Because podman's container engine needs to run on Linux, to provide support for macOS and Windows, some form of Linux environment is needed. To address this, podman makes use of virtualisation environments available on Windows or macOS to start a Linux virtual machine (VM) behind the scenes. It then provides a native command line tool for macOS and Windows that can communicate with the podman engine inside the Linux VM in a (mostly) transparent way.

You can control this underlying virtual machine via the `podman machine` command. On Linux, the use of the `podman machine` command is not necessary since podman runs natively.

On macOS, recent versions of podman (v5.0+) will use the native Apple hypervisor to provision the podman machine. _If you're using an older version of macOS, e.g. macOS 12 (Monterey), this will not work and you'll need to use an older version of podman ([v4.9.3](https://github.com/containers/podman/releases/tag/v4.9.3)) which will use the [qemu](https://www.qemu.org/) backend._

On Windows, there are two options, you can either use the Windows Subsystem for Linux v2 (WSL2) as the platform on which to run the podman VM, or you can use Hyper-V.

### So why aren't you just using Docker?!

Docker has become an incredibly popular and widely used container platform. However, while the open source [containerd](https://github.com/containerd/containerd) container runtime and [Docker Engine](https://docs.docker.com/engine/) underpin Docker, [Docker Desktop](https://docs.docker.com/desktop/), the most commonly used and most straightforward to install cross-platform solution for Docker, which includes these tools, is a commercial package. Docker Desktop also bundles a range of additional tools and functionality (some of which can also be obtained individually as open source products) that are important when making more advanced use of containers. More generally, the straightfoward installation process and ease of use associated with Docker Desktop, when compared to the manual approach of installing and managing the associated open source tools, make Docker Desktop a much more practical solution for Docker users.

Nonetheless, the associated cost can make the use of Docker in a research environment impractical, especially where other free, open source solutions exist. The [license](https://docs.docker.com/subscription/desktop-license/) for Docker Desktop has, in the past, highlighted free use for training and education and various other cases but a number of updates have been made and things do change. While the current license terms mean that free use of Docker Desktop may be acceptable for some academic/teaching use cases (please see [the license](https://docs.docker.com/subscription/desktop-license/)), we have opted to focus on covering a fully free open source solution for this session.

### Installing podman

You can install podman on Linux, macOS and Windows. Note that for this session, we're not going to be installing and using Podman Desktop. We're using the underlying podman tool and it's a associated command line tool (the podman CLI).

Podman Desktop is a desktop graphical user interface (GUI) tool for controlling podman containers. However it also supports controlling a range of other containters via plugins for different container engines and runtimes.

You can work from podman's installation instructions at [https://podman.io/docs/installation](https://podman.io/docs/installation). However, we also provide a little further information in this section of the session information.

##### Getting podman

**NOTE:** _On macOS, recent versions of podman (v5.0+) will use the native Apple hypervisor to provision the podman machine. If you're using an older version of macOS, e.g. macOS 12 (Monterey), this will not work and you'll need to use an older version of podman ([v4.9.3](https://github.com/containers/podman/releases/tag/v4.9.3)) which will use the qemu backend._

You can find the latest release of podman (currently v5.3.0) on the [releases page](https://github.com/containers/podman/releases/) in the GitHub repository. Unless you need to install an older version (_e.g. v4.9.3 for which you can find the link above_), pick the latest release and scroll down past the list of "Features", "Changes" and "Bugfixes" to the "Assets" section where you'll find a list of files that can be downloaded. Select the relevant file based on your operating system and machine type:

**Windows:** `podman-5.3.0-setup.exe` <br/>
**macOS (Intel):** `podman-installer-macos-amd64.pkg` <br/>
**macOS (Apple Silicon):** `podman-installer-macos-arm64.pkg`

**Linux:** Use the [Linux install instructions in the podman docs](https://podman.io/docs/installation#installing-on-linux) to install via your distribution's package manager.

###### macOS

Go ahead and run the `.pkg` file that you've downloaded in order to install podman. Assuming everything completes successfully, open a new terminal window and run `podman --version` to check that the podman command is available on the command line.

At this point we also strongly advise that you run `podman machine init` to set up the podman VM so that podman is ready to use. **NOTE:** _Running the podman machine init command will trigger the download of the podman virtual machine image which may be quite large - several hundred megabytes or more depending on the VM backend you're using._

At this point you can run `podman machine start` to try and start up the podman machine. If this works succesfully, you are now ready to use podman. We recommend you now stop the podman VM if you have no intention of using it right away, using `podman machine stop`.

###### Windows

For Windows, there are two options for which underlying virtualisation framework to use to run your podman VM - you can either use the Windows Subsystem for Linux v2 (WSL2) or you can use Hyper-V. In either case, if you're not already using the selected framework you may need to enable some additional options in Windows. The following [installing podman](https://podman-desktop.io/docs/installation/windows-install#installing-podman) page, while targeted at installation of Podman Desktop, which we are not using, provides some useful information on how to enable WSL2 or Hyper-V on your system if you haven't already enabled/used one of these tools.

At this point you can run the `.exe` podman installer file that you downloaded from GitHub and follow the instructions to install podman.

If the installation completes sucessfully open a new command line (CMD) or PowerShell window and run `podman --version` to check that the podman command is available on the command line.

We strongly advise that you now also run `podman machine init` to set up the podman VM so that podman is ready to use. **NOTE:** _Running the podman machine init command will trigger the download of the podman virtual machine image which may be quite large - several hundred megabytes or more depending on the VM backend you're using._

At this point you can run `podman machine start` to try and start up the podman machine. If this works succesfully, you are now ready to use podman. We recommend you now stop the podman VM if you have no intention of using it right away, using `podman machine stop`.