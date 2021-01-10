# Unpin and Remove all IPFS content from the machine

I was wishing to just fetch\(download/add\) the files that I want instead of automatically hosting all contents out there\(and "earn" some filecoin~\). While when I started the IPFS Desktop, it automatically started downloading some data, thus I want to remove all these files.

And there are some commands that need to be figured out "Unpin" "repo gc"

[https://stackoverflow.com/questions/43118022/how-do-i-unpin-and-remove-all-ipfs-content-from-my-machine](https://stackoverflow.com/questions/43118022/how-do-i-unpin-and-remove-all-ipfs-content-from-my-machine)

```text
# to unpin all added content:

$ ipfs pin ls --type recursive | cut -d' ' -f1 | xargs -n1 ipfs pin rm

# then optionally run storage garbage collection to actually remove things:

$ ipfs repo gc
```

