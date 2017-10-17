# govendorx
A small wrapper to govendor that enables you to list required missing dependencies 

govendox wrapps govendor. It adds functionality of listing and fetching missing but required 
dependencies. `govendorx list +r` returns a subset of `govendorx list +m`. 
It returns the missing decencies that are needed by the program and can be fetched 
through an url.


## Install 
```
go get -u github.com/kardianos/govendor
curl https://raw.githubusercontent.com/modfin/govendorx/master/govendorx > /usr/local/bin/govendorx
chmod +x /usr/local/bin/govendorx
```

## Motivation
In example, when mounting/symlinking a kit repo in the vendors folder and not wanting to pull 
all the external decencies of the repo. This enables you to only pull external decencies of 
used sub packages of the kit repo. This is useful in a useful when developing in a docker context 
and kit development is done i parallel.

## Usage of extension to govendor
```
> govendorx list +r
> govendorx list +required
> govendorx fetch +r
```
