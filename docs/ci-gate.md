# Warunkowe CI

## Wspólna nazwa required

PR #20 był próbą porównawczą, bez merge. Pozostałe wymagane checki aplikacji były zielone.

| Próba | Wyniki required | Merge | Commit |
| --- | --- | --- | --- |
| zero |  | BLOCKED | [6d15f90](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/6d15f90c3bef5a009a6b47a484f3f87c125eb106) |
| one | success | CLEAN | [d578d50](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/d578d509f795d4e4b7447437a670412301a8258c) |
| two-pending | pending + success | BLOCKED | [add3dc3](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/add3dc34f36ea4b20e93e3fa251c5e5dc471a835) |
| two-success | success + success | CLEAN | [add3dc3](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/add3dc34f36ea4b20e93e3fa251c5e5dc471a835) |
| two-failure | failure + success | BLOCKED | [7cf4430](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/7cf443048eb6f5213fc66fdb350051a65b1720fc) |
| two-fixed | success + success | CLEAN | [ab9cdb5](https://github.com/shihan-project/tdo-2026-lab-02-s30576-pj/commit/ab9cdb5edec258dd722635b4b93b5215268edc9c) |

Dane: [porównanie](evidence/required-comparison-stage19.json). Tymczasowe workflow usunięto po próbie.

## Gate

Detekcja musi się udać, a flagi mają mieć wartość true lub false. Wymagany komponent musi zakończyć się success; niewymagany musi być skipped. Pozostałe kombinacje odrzucane.

Przed wdrożeniem sprawdzono [11 przypadków kontraktu](evidence/gate-local-contract.json), w tym cancelled, brak flagi i nieoczekiwane pominięcie.

