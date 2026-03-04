## Docker Version

```

Client:
Version:           29.2.1
API version:       1.53
Go version:        go1.25.6
Git commit:        a5c7197
Built:             Mon Feb  2 17:20:16 2026
OS/Arch:           windows/amd64
Context:           desktop-linux

Server: Docker Desktop 4.63.0 (220185)

```

## Docker Hello World
```bash
docker run hello-world

```

```
Hello from Docker!
This message shows that your installation appears to be working correctly.

```

## PostgreSQL Container Commands

**Stop the container:**

```bash
docker stop pg-prework

```

```
pg-prework

```

**Restart the container:**

```bash
docker restart pg-prework

```

```
pg-prework

```

**Check the logs:**

```bash
docker logs pg-prework

```

```
PostgreSQL Database directory appears to contain a database; Skipping initialization

2026-03-04 08:11:33.383 UTC [1] LOG:  starting PostgreSQL 15.17 on x86_64-pc-linux-musl, compiled by gcc (Alpine 15.2.0) 15.2.0, 64-bit
2026-03-04 08:11:33.383 UTC [1] LOG:  listening on IPv4 address "0.0.0.0", port 5432
2026-03-04 08:11:33.383 UTC [1] LOG:  listening on IPv6 address "::", port 5432
2026-03-04 08:11:33.390 UTC [1] LOG:  listening on Unix socket "/var/run/postgresql/.s.PGSQL.5432"
2026-03-04 08:11:33.402 UTC [29] LOG:  database system was shut down at 2026-03-04 08:10:41 UTC
2026-03-04 08:11:33.416 UTC [1] LOG:  database system is ready to accept connections

```

```

```bash
git add docs/docker-notes.md
git commit -m "fix: format docker notes for autograder"
git push origin pr-08-docker

```
