# TODO

## Architecture

- Base backage name should be rather something like `io.github.dadikovi.library.shelf`
- Currently all shelf change triggers the recalculation of all statistics. If the requirement is not instantaneous consistency, this could be optimized. 

## Dev

- Implement missing statistics
- Lombok project is not used right now, it could simplify some pojos.
- Jhipster generates constant hashCode implementations for DB entities, so we should not use them as hashmap keys.
- Checkstyle, pmd, sonar checks

## Ops

- Write documentation
- Currently to start the application all services must be built first in its repository. Images could be stored in a docker registry, so this step could be eliminated.
