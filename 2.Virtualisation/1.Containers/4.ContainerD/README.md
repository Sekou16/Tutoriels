# Container D

### :a: Architecture

<img src="https://containerd.io/img/architecture.png" width="891" height="540"></img>


### :open_book: Docker-CLI, dockerd, containerd, runc, containerd-shim, ... WTH

:star: [=> docker components explained](http://alexander.holbreich.org/docker-components-explained)


## :b: ContainerD Commands

:closed_book: https://www.mankier.com/package/containerd

### :zero: From LinuxKit/Darwin

https://sweetcode.io/getting-started-with-containerd/

```
docker-desktop:~# ctr --namespace services.linuxkit container ls
CONTAINER                IMAGE    RUNTIME                           
acpid                    -        io.containerd.runtime.v1.linux    
diagnose                 -        io.containerd.runtime.v1.linux    
docker                   -        io.containerd.runtime.v1.linux    
host-timesync-daemon     -        io.containerd.runtime.v1.linux    
kmsg                     -        io.containerd.runtime.v1.linux    
sntpc                    -        io.containerd.runtime.v1.linux    
socks                    -        io.containerd.runtime.v1.linux    
trim-after-delete        -        io.containerd.runtime.v1.linux    
vpnkit-forwarder         -        io.containerd.runtime.v1.linux    
write-and-rotate-logs    -        io.containerd.runtime.v1.linux    
```

```
docker-desktop:~# ctr --namespace services.linuxkit container info docker | more
{
    "ID": "docker",
    "Labels": null,
    "Image": "",
    "Runtime": {
        "Name": "io.containerd.runtime.v1.linux",
        "Options": null
    },
    "SnapshotKey": "",
    "Snapshotter": "",
    "CreatedAt": "2020-01-15T14:16:08.816898999Z",
    "UpdatedAt": "2020-01-15T14:16:08.816898999Z",
    "Extensions": null,
    "Spec": {
        "ociVersion": "1.0.1",
        "process": {
            "user": {
                "uid": 0,
                "gid": 0
            },
            "args": [
                "/usr/local/bin/docker-init",
                "/usr/bin/entrypoint.sh"
```

### :one: From docker-machine ssh/HyperV
   
```
docker@CB-HYPERV:~$ sudo ctr --address /var/run/docker/containerd/containerd.sock container ls
CONTAINER    IMAGE    RUNTIME
```

```
docker@CB-HYPERV:~$ sudo ctr --address /var/run/docker/containerd/containerd.sock image ls
REF TYPE DIGEST SIZE PLATFORMS LABELS
```

# Références 


## Container RunTime

https://www.ianlewis.org/en/container-runtimes-part-1-introduction-container-r

https://medium.com/@alenkacz/whats-the-difference-between-runc-containerd-docker-3fc8f79d4d6e
