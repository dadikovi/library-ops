# TODO

## Architecture

- `library-stats` depends on `library-shelf`. This should be avoided in microservice architecture, however, they both operate on the same data set and I also wanted to avoid using shared database (which I think is even worse).

## Ops

- Currently to start the application all services must be built first in its repository. Images could be stored in a docker registry, so this step could be eliminated.
