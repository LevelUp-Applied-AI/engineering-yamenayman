docker version
Client:
 Version:           29.2.1
 API version:       1.53
 Go version:        go1.25.6
 Git commit:        a5c7197
 Built:             Mon Feb  2 17:20:16 2026
 OS/Arch:           windows/amd64
 Context:           desktop-linux

Server: Docker Desktop 4.63.0 (220185)
 Engine:
  Version:          29.2.1
  API version:      1.53 (minimum version 1.44)
  Go version:       go1.25.6
  Git commit:       6bc6209
  Built:            Mon Feb  2 17:17:24 2026
  OS/Arch:          linux/amd64
  Experimental:     false
 containerd:
  Version:          v2.2.1
  GitCommit:        dea7da592f5d1d2b7755e3a161be07f43fad8f75
 runc:
  Version:          1.3.4
  GitCommit:        v1.3.4-0-gd6d73eb8
 docker-init:
  Version:          0.19.0
  GitCommit:        de40ad0

# #######################################################################

 docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
17eec7bbc9d7: Pull complete
ea52d2000f90: Download complete
Digest: sha256:ef54e839ef541993b4e87f25e752f7cf4238fa55f017957c2eb44077083d7a6a
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

To generate this message, Docker took the following steps:
 1. The Docker client contacted the Docker daemon.
 2. The Docker daemon pulled the "hello-world" image from the Docker Hub.
    (amd64)
 3. The Docker daemon created a new container from that image which runs the
    executable that produces the output you are currently reading.
 4. The Docker daemon streamed that output to the Docker client, which sent it
    to your terminal.

To try something more ambitious, you can run an Ubuntu container with:
 $ docker run -it ubuntu bash

Share images, automate workflows, and more with a free Docker ID:
 https://hub.docker.com/

For more examples and ideas, visit:
 https://docs.docker.com/get-started/

# ###########################################################################################################
paste output of:  docker stop pg-prework
pg-prework

paste output of: 



paste output of: docker logs pg-prework
The files belonging to this database system will be owned by user "postgres".
This user must also own the server process.

The database cluster will be initialized with locale "en_US.utf8".
The default database encoding has accordingly been set to "UTF8".
The default text search configuration will be set to "english".

Data page checksums are disabled.

fixing permissions on existing directory /var/lib/postgresql/data ... ok
creating subdirectories ... ok
selecting dynamic shared memory implementation ... posix
selecting default max_connections ... 100
selecting default shared_buffers ... 128MB
selecting default time zone ... UTC
creating configuration files ... ok
running bootstrap script ... ok
sh: locale: not found
2026-03-04 08:07:27.310 UTC [35] WARNING:  no usable system locales were found
performing post-bootstrap initialization ... ok
initdb: warning: enabling "trust" authentication for local connections
initdb: hint: You can change this by editing pg_hba.conf or using the option -A, or --auth-local and --auth-host, the next time you run initdb.
syncing data to disk ... ok


Success. You can now start the database server using:

    pg_ctl -D /var/lib/postgresql/data -l logfile start

waiting for server to start....2026-03-04 08:07:28.139 UTC [41] LOG:  starting PostgreSQL 15.17 on x86_64-pc-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-03-04 08:07:28.143 UTC [41] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 08:07:28.153 UTC [44] LOG:  database system was shut down at 2026-03-04 08:07:27 UTC
2026-03-04 08:07:28.163 UTC [41] LOG:  database system is ready to accept connections
 done
server started

/usr/local/bin/docker-entrypoint.sh: ignoring /docker-entrypoint-initdb.d/*

waiting for server to shut down....2026-03-04 08:07:28.254 UTC [41] LOG:  received fast shutdown request
2026-03-04 08:07:28.259 UTC [41] LOG:  aborting any active transactions
2026-03-04 08:07:28.263 UTC [41] LOG:  background worker "logical replication launcher" (PID 47) exited with exit code 1
2026-03-04 08:07:28.264 UTC [42] LOG:  shutting down
2026-03-04 08:07:28.268 UTC [42] LOG:  checkpoint starting: shutdown immediate
2026-03-04 08:07:28.288 UTC [42] LOG:  checkpoint complete: wrote 3 buffers (0.0%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.007 s, sync=0.002 s, total=0.024 s; sync files=2, longest=0.002 s, average=0.001 s; distance=0 kB, estimate=0 kB
2026-03-04 08:07:28.296 UTC [41] LOG:  database system is shut down
 done
server stopped

PostgreSQL init process complete; ready for start up.

2026-03-04 08:07:28.388 UTC [1] LOG:  starting PostgreSQL 15.17 on x86_64-pc-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-03-04 08:07:28.388 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-03-04 08:07:28.388 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-03-04 08:07:28.394 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 08:07:28.399 UTC [55] LOG:  database system was shut down at 2026-03-04 08:07:28 UTC
2026-03-04 08:07:28.406 UTC [1] LOG:  database system is ready to accept connections
2026-03-04 08:10:41.024 UTC [1] LOG:  received fast shutdown request
2026-03-04 08:10:41.029 UTC [1] LOG:  aborting any active transactions
2026-03-04 08:10:41.034 UTC [1] LOG:  background worker "logical replication launcher" (PID 58) exited with exit code 1
2026-03-04 08:10:41.036 UTC [53] LOG:  shutting down
2026-03-04 08:10:41.040 UTC [53] LOG:  checkpoint starting: shutdown immediate
2026-03-04 08:10:41.062 UTC [53] LOG:  checkpoint complete: wrote 43 buffers (0.3%); 0 WAL file(s) added, 0 removed, 0 recycled; write=0.006 s, sync=0.007 s, total=0.027 s; sync files=11, longest=0.004 s, average=0.001 s; distance=252 kB, estimate=252 kB
2026-03-04 08:10:41.071 UTC [1] LOG:  database system is shut down

PostgreSQL Database directory appears to contain a database; Skipping initialization

2026-03-04 08:11:33.383 UTC [1] LOG:  starting PostgreSQL 15.17 on x86_64-pc-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-03-04 08:11:33.383 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-03-04 08:11:33.383 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-03-04 08:11:33.390 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 08:11:33.402 UTC [29] LOG:  database system was shut down at 2026-03-04 08:10:41 UTC
2026-03-04 08:11:33.416 UTC [1] LOG:  database system is ready to accept connections
