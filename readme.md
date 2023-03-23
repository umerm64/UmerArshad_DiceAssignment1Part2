docker ps
CONTAINER ID   IMAGE     COMMAND           CREATED         STATUS         PORTS                                       NAMES
1bea31c633c1   task1     "python app.py"   2 minutes ago   Up 2 minutes   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   goofy_cohen

docker stop
goofy_cohen

docker rm
goofy_cohen

docker logs
 * Serving Flask app 'app' (lazy loading)
 * Environment: production
[31m   WARNING: This is a development server. Do not use it in a production deployment.[0m
[2m   Use a production WSGI server instead.[0m
 * Debug mode: on
[31m[1mWARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.[0m
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:5000
 * Running on http://172.17.0.2:5000
[33mPress CTRL+C to quit[0m
 * Restarting with stat
 * Debugger is active!
 * Debugger PIN: 853-391-461
172.17.0.1 - - [23/Mar/2023 15:13:20] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [23/Mar/2023 15:13:21] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [23/Mar/2023 15:13:21] "GET / HTTP/1.1" 200 -

docker inspect
[
    {
        "Id": "d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237",
        "Created": "2023-03-23T15:13:06.826177995Z",
        "Path": "python",
        "Args": [
            "app.py"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 33357,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-03-23T15:13:07.140148454Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:836d6bc1d9a6faadd0e21a086c489244968ac63e65ef6930d0c2162808a04f6a",
        "ResolvConfPath": "/var/lib/docker/containers/d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237/hostname",
        "HostsPath": "/var/lib/docker/containers/d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237/hosts",
        "LogPath": "/var/lib/docker/containers/d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237/d12e02d5be9538f61e9c23e5d096d61a1ca109e18b1df2b89dd7d90091f21237-json.log",
        "Name": "/great_buck",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "5000/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "5000"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                50,
                101
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "host",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": false,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/af40aeb4b99af681e4b431468ac3af128903fe5ca01f6668cd32cc4278e7cc74-init/diff:/var/lib/docker/overlay2/txfksgo6j94c2zuevbn53dmiu/diff:/var/lib/docker/overlay2/cpxat0uk35kozqio18vnp2wl2/diff:/var/lib/docker/overlay2/8hzzzbmih4wlagod7hi6bfrxo/diff:/var/lib/docker/overlay2/qb0fzgwt70oyqun7dw3vqcmr3/diff:/var/lib/docker/overlay2/f4811de57ed64a6b75c9d92745b21061a003b196522a29e5a1865ed9ea88b95f/diff:/var/lib/docker/overlay2/653ef2480b872ece568fbe5f871ff071d35765011e458a2d4e5ef723bf7b5cd6/diff:/var/lib/docker/overlay2/47e376a57df618acb87ecc80cb185431397b714233954bac1928f242bde225f0/diff:/var/lib/docker/overlay2/4ebfe19608d122fdfc2ce8a30bbf6323e709a7f92e178272cac972d8d43bb044/diff:/var/lib/docker/overlay2/0d14c02d1e8c02fad755e35f40929acd7ec701489abd8bf858cc22b79bb81689/diff",
                "MergedDir": "/var/lib/docker/overlay2/af40aeb4b99af681e4b431468ac3af128903fe5ca01f6668cd32cc4278e7cc74/merged",
                "UpperDir": "/var/lib/docker/overlay2/af40aeb4b99af681e4b431468ac3af128903fe5ca01f6668cd32cc4278e7cc74/diff",
                "WorkDir": "/var/lib/docker/overlay2/af40aeb4b99af681e4b431468ac3af128903fe5ca01f6668cd32cc4278e7cc74/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "d12e02d5be95",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": false,
            "AttachStderr": false,
            "ExposedPorts": {
                "5000/tcp": {}
            },
            "Tty": true,
            "OpenStdin": true,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "LANG=C.UTF-8",
                "GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568",
                "PYTHON_VERSION=3.8.16",
                "PYTHON_PIP_VERSION=22.0.4",
                "PYTHON_SETUPTOOLS_VERSION=57.5.0",
                "PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d5cb0afaf23b8520f1bbcfed521017b4a95f5c01/public/get-pip.py",
                "PYTHON_GET_PIP_SHA256=394be00f13fa1b9aaa47e911bdb59a09c3b2986472130f30aa0bfaf7f3980637"
            ],
            "Cmd": [
                "app.py"
            ],
            "Image": "task1",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": [
                "python"
            ],
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "7ca5510dce359bebac6971be159926fb25290d388f1edc446fcc58c90e64b3dc",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "5000/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "5000"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "5000"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/7ca5510dce35",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "bb02c73d0c0dff5df907275cac99c0f8b2e057f14e8c1618a28ad227c65d8fd8",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "bcaeedc790603aecde375d806b8afb88f0b9f4af5d25323c976853e924b60536",
                    "EndpointID": "bb02c73d0c0dff5df907275cac99c0f8b2e057f14e8c1618a28ad227c65d8fd8",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

docker exec
/app
              total        used        free      shared  buff/cache   available
Mem:        3994720     2762672      267768       67968      964280      901748
Swap:        969960      477952      492008
Thu Mar 23 15:15:23 UTC 2023

docker attach great_buck 
172.17.0.1 - - [23/Mar/2023 15:16:18] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [23/Mar/2023 15:16:19] "GET / HTTP/1.1" 200 -

docker attach great_buck 
172.17.0.1 - - [23/Mar/2023 15:16:18] "GET / HTTP/1.1" 200 -
172.17.0.1 - - [23/Mar/2023 15:16:19] "GET / HTTP/1.1" 200 -

docker cp readme.md great_buck:/app/
Preparing to copy...
Copying to container - 12.29kB
Successfully copied 12.29kB to great_buck:/app/

docker stats great_buck
CONTAINER ID   NAME         CPU %     MEM USAGE / LIMIT    MEM %     NET I/O       BLOCK I/O   PIDS
d12e02d5be95   great_buck   0.10%     37.95MiB / 3.81GiB   0.97%     3.64kB / 0B   0B / 0B     5

docker top great_buck 
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                36143               36113               0                   20:18               ?                   00:00:00            python app.py
root                36179               36143               0                   20:18               ?                   00:00:00            /usr/local/bin/python /app/app.py
root                36248               36113               0                   20:18               pts/1               00:00:00            sh
root                36450               36113               0                   20:18               ?                   00:00:00            /bin/sh

docker start great_buck
great_buck

docker pause great_buck 
great_buck
CONTAINER ID   IMAGE     COMMAND           CREATED         STATUS                  PORTS                                       NAMES
d12e02d5be95   task1     "python app.py"   7 minutes ago   Up 2 minutes (Paused)   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   great_buck

docker unpause great_buck 
great_buck
CONTAINER ID   IMAGE     COMMAND           CREATED         STATUS         PORTS                                       NAMES
d12e02d5be95   task1     "python app.py"   7 minutes ago   Up 2 minutes   0.0.0.0:5000->5000/tcp, :::5000->5000/tcp   great_buck

docker rename great_buck task2

docker wait task2 
0

docker port task2 
5000/tcp -> 0.0.0.0:5000
5000/tcp -> [::]:5000

docker update task2 --restart always
task2

docker restart task2
task2
