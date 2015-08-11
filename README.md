
# rtop-bot

*rtop-bot* is a bot front-end to *rtop*.

*rtop* can connect over SSH to Linux systems and display their vital system
metrics without needing any agent on the target system. *rtop-bot* can do
this when asked to, over HipChat, and report the results to the chat room.
*rtop-bot* is independent of *rtop*.

*rtop-bot* has to be self-hosted. You can run it on a machine within your
secure network from which it can SSH to target systems. When run, it will
connect to a HipChat room as the user you specify, and listen for mentions:

    you     | @rtop-bot status some.host
    rtop-bot| [some.host] up 34d 20h 1m 51s, load 0.08 0.03 0.05, procs 1 running of 131 total
    rtop-bot| [some.host] mem: 45.55 MiB of 489.57 MiB free, swap 0 bytes of 0 bytes free
    rtop-bot| [some.host] fs /: 16.18 GiB of 18.55 GiB free

*rtop-bot*'s [home page](http://www.rtop-monitor.org/rtop-bot) has more
information and screenshots!

## build

*rtop-bot* is written in [go](http://golang.org/), and requires Go version 1.2
or higher. To build, *go get* it:

    go get github.com/rapidloop/rtop-bot

You should find the binary *rtop-bot* under *$GOPATH/bin* when the command
completes. There are no runtime dependencies or configuration needed.

## contribute

Pull requests welcome. Keep it simple.

## changelog
* 11-Aug-2015: first public release
