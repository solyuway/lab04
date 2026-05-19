# Laboratory Work No. 4 - Continuous Integration

## Build Status

### GitHub Actions

[![CI](https://github.com/solyuway/lab04/actions/workflows/ci.yml/badge.svg)](https://github.com/solyuway/lab04/actions/workflows/ci.yml)

### Travis CI

[![Build Status](https://travis-ci.com/solyuway/lab04.svg?branch=master)](https://travis-ci.com/solyuway/lab04)

## Description

This project demonstrates continuous integration setup using:
- Travis CI
- GitHub Actions

## Building
\```bash
cmake -H. -B_build -DCMAKE_INSTALL_PREFIX=_install
cmake --build _build
cmake --build _build --target install
\```


