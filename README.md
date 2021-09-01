# moby building

## Windows

### Prerequisites

1. windmc
    - windmc is a part of binutils
2. make

You could get make from gnuwin32, but i couldn't find windmc there.
So - just install cygwin - http://cygwin.com/install.html

remember to select binutils and make,
gcc g++ and similar are welcome too

3. golang
    - https://golang.org/


### Build

0. Open powershell
1. cd to moby dir
2. Initialize go

        go mod init
3. run

        .\hack\make.ps1
    - need fixes in powershell scripts as double quoutes used in .go-autogen.ps1 are failing on powershell 7 with following error:

            windres: hack/make/.resources-windows/common.rc:23: syntax error

