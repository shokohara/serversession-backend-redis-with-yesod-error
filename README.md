First, I got below error.

```
Error: While constructing the build plan, the following exceptions were encountered:

In the dependencies for serversession-backend-redis-with-yesod-error-0.0.0:
    serversession-backend-redis must match -any, but the stack configuration has no specified version
                                (latest applicable is 1.0.1)

Recommended action: try adding the following to your extra-deps in /home/sho/src/serversession-backend-redis-with-yesod-error/stack.yaml:
- serversession-backend-redis-1.0.1

You may also want to try the 'stack solver' command
Plan construction failed.
sho@helium:~/src/serversession-backend-redis-with-yesod-error$
```

So, I added that line to extra-deps, and then I hit `stack build`, then I got below error.

```
sho@helium:~/src/serversession-backend-redis-with-yesod-error$ stack build

Error: While constructing the build plan, the following exceptions were encountered:

In the dependencies for serversession-backend-redis-1.0.1:
    hedis-0.9.7 must match ==0.6.* (latest applicable is 0.6.10)
needed due to serversession-backend-redis-with-yesod-error-0.0.0 -> serversession-backend-redis-1.0.1

Plan construction failed.
```

