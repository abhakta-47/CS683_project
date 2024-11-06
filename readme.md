## Setup repo
- `git clone <repo-link>`
- `git submodule update --init --recursive`

## Multi2Sim guides
- run multi2sim using docker `docker run --rm -it  multi2sim/multi2sim:latest bash`
- x86 config `docker run --rm -it multi2sim/multi2sim:latest m2s --x86-help`
- memory config `docker run --rm -it multi2sim/multi2sim:latest m2s --mem-help`

## Benchmarks
### Parsec
### Splash2
### Sepc OMPM 2001
### FFTW
### Server applications
- SPEC jbb
- Apache HTTP server
- MySQL TPC-C
- MySQL TPC-E
- MySQL TPC-H