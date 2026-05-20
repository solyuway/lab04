# Laboratory Work No. 4 - Continuous Integration

## Build Status

### Travis CI

[![Build Status](https://travis-ci.com/solyuway/lab04.svg?branch=master)](https://travis-ci.com/solyuway/lab04)

### AppVeyor

[![Build status](https://ci.appveyor.com/api/projects/status/4yrolspg59knj362/branch/master?svg=true)](https://ci.appveyor.com/project/solyuway/lab04)

### GitHub Actions (дополнительно)

[![GitHub Actions](https://github.com/solyuway/lab04/actions/workflows/ci.yml/badge.svg)](https://github.com/solyuway/lab04/actions)

## Description

This project demonstrates continuous integration setup using:

- **Travis CI** (Linux: gcc and clang)
- **AppVeyor** (Windows: VS 2019/2022, x64/x86, Debug/Release)
- **GitHub Actions** (optional)

## Building

```bash
mkdir build && cd build
cmake .. -DCMAKE_INSTALL_PREFIX=_install
cmake --build .
cmake --build . --target install
