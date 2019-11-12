# Data Sharing and Collaboration with DVC

Like Git, DVC facilitates collaboration and data sharing on a distributed
environment. It makes it easy to consistently get all your data files and
directories to any machine, along with matching source code.

![](/static/img/model-sharing-digram.png)

There are several ways to setup data sharing with DVC. We will discuss the most
common scenarios.

- [Sharing Data Through a Remote DVC Storage](/doc/user-guide/data-sharing/remote-storage)

  This is the recommended and the most common case of data sharing. In this case
  we setup a [remote storage](/doc/command-reference/remote) on a data storage
  provider, to store data files online, where others can reach them. Currently
  DVC supports Amazon S3, Google Cloud Storage, Microsoft Azure Blob Storage,
  SSH, HDFS, and other remote locations, and the list is constantly growing.

- [Using Local Storage on a Shared Development Server](/doc/user-guide/data-sharing/shared-server)

  Some teams may prefer using a single shared machine to run their experiments.
  This allows them to have better resource utilization such as the ability to
  use multiple GPUs, etc. In this case we can use a local data storage, which
  allows the team to store and share data very efficiently, with no duplication
  of data files and instantaneous transfer.

- [Sharing Data Through a Mounted DVC Storage](/doc/user-guide/data-sharing/mounted-storage)

  If the data storage server (or provider) has a protocol that is not supported
  yet by DVC, but it allows us to mount a remote directory on the local
  filesystem, then we can still make a setup for data sharing with DVC. This
  case might be useful for example when the data files are located on a
  network-attached storage (NAS) and can be accessed through protocols like NFS,
  Samba, SSHFS, etc.

- [Sharing Data Through a Synchronized DVC Storage](/doc/user-guide/data-sharing/synched-storage)

  There are cloud data storage providers that are not supported yet by DVC. But
  this does not mean that we cannot use them to share data with the help of DVC.
  If it is possible to synchronize a local directory with a remote one (which is
  supported by almost all storage providers), then we are good to go. We can
  make a setup that allows us to share DVC data.