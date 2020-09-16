# Snapd must die

Snaps seem like a good idea. I like the idea of application-segregation.

But the `snapd` daemon started writing at 300kb/s to my memory card on 3 of my 4
Raspberry Pis.

I'm not currently using any snaps and memory cards don't like being written to
constantly.

Example of what was being written:

```
[pid 53577] openat(AT_FDCWD, "/var/lib/snapd/state.json.sfM0kXVR1VHx~", O_WRONLY|O_CREAT|O_EXCL|O_TRUNC|O_CLOEXEC, 0600) = 3
[pid 53577] write(3, "{\"data\":{\"auth\":{\"last-id\":0,\"us"..., 49776) = 49776
[pid 53577] openat(AT_FDCWD, "/var/lib/snapd", O_RDONLY|O_CLOEXEC) = 9
[pid 53577] newfstatat(AT_FDCWD, "/var/lib/snapd/state.json", {st_mode=S_IFREG|0600, st_size=49819, ...}, AT_SYMLINK_NOFOLLOW) = 0
[pid 53577] renameat(AT_FDCWD, "/var/lib/snapd/state.json.sfM0kXVR1VHx~", AT_FDCWD, "/var/lib/snapd/state.json") = 0
[pid 53577] openat(AT_FDCWD, "/var/lib/snapd/state.json.5g6YkBCMYST4~", O_WRONLY|O_CREAT|O_EXCL|O_TRUNC|O_CLOEXEC, 0600) = 3
[pid 53577] write(3, "{\"data\":{\"auth\":{\"last-id\":0,\"us"..., 49819) = 49819
[pid 53577] openat(AT_FDCWD, "/var/lib/snapd", O_RDONLY|O_CLOEXEC) = 9
[pid 53577] newfstatat(AT_FDCWD, "/var/lib/snapd/state.json", {st_mode=S_IFREG|0600, st_size=49776, ...}, AT_SYMLINK_NOFOLLOW) = 0
[pid 53577] renameat(AT_FDCWD, "/var/lib/snapd/state.json.5g6YkBCMYST4~", AT_FDCWD, "/var/lib/snapd/state.json") = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic/active",  <unfinished ...>
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic/active", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] read(9, "type: model\nauthority-id: generi"..., 1469) = 957
[pid  1373] <... read resumed>"", 512)  = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148/active",  <unfinished ...>
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148/active", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] read(9, "type: serial\nauthority-id: gener"..., 2335) = 1823
[pid  1373] <... read resumed>"", 512)  = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic/active",  <unfinished ...>
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/model/16/generic/generic-classic/active", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] <... read resumed>"type: model\nauthority-id: generi"..., 1469) = 957
[pid  1373] <... read resumed>"", 512)  = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148/active",  <unfinished ...>
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/assertions/asserts-v0/serial/generic/generic-classic/8e2a4c60-95a1-4bc1-84b3-d4a01fa01148/active", O_RDONLY|O_CLOEXEC <unfinished ...>
[pid  1373] read(9, "type: serial\nauthority-id: gener"..., 2335) = 1823
[pid  1373] <... read resumed>"", 512)  = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/state.json.YW3RXlJQnyfc~", O_WRONLY|O_CREAT|O_EXCL|O_TRUNC|O_CLOEXEC, 0600) = 3
[pid  1373] write(3, "{\"data\":{\"auth\":{\"last-id\":0,\"us"..., 49776) = 49776
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd", O_RDONLY|O_CLOEXEC) = 9
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/state.json", {st_mode=S_IFREG|0600, st_size=49819, ...}, AT_SYMLINK_NOFOLLOW) = 0
[pid  1373] renameat(AT_FDCWD, "/var/lib/snapd/state.json.YW3RXlJQnyfc~", AT_FDCWD, "/var/lib/snapd/state.json") = 0
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd/state.json.7456vdKY0XQK~", O_WRONLY|O_CREAT|O_EXCL|O_TRUNC|O_CLOEXEC, 0600) = 3
[pid  1373] write(3, "{\"data\":{\"auth\":{\"last-id\":0,\"us"..., 49819) = 49819
[pid  1373] openat(AT_FDCWD, "/var/lib/snapd", O_RDONLY|O_CLOEXEC) = 9
[pid  1373] newfstatat(AT_FDCWD, "/var/lib/snapd/state.json", {st_mode=S_IFREG|0600, st_size=49776, ...}, AT_SYMLINK_NOFOLLOW) = 0
[pid  1373] renameat(AT_FDCWD, "/var/lib/snapd/state.json.7456vdKY0XQK~", AT_FDCWD, "/var/lib/snapd/state.json") = 0
```

It appears to me that snapd got locked into some sort unrecoverable loop.

Restarting the snapd daemon did not help.

Since I'm not currently using any snaps and I don't like the idea of services
that I'm not using running anywhere I've killed snapd service on all my RP4's

## Killing snapd is harder than it should be

Turns out Ubuntu really wants snapd to be a thing and so it is difficult to kill
this service.

I had to stop, disable, and then _mask_ the service to keep it down.

```
$ systemctl stop snapd.service
$ systemctl disable snapd.service
$ systemctl mask snapd.service
```

Then I had to kill the daemon manually

```
$ ps -efw | grep snapd
$ kill <snapd-pid>
```

## Lessons learned

`strace -f -p <pid>` is awesome way to figure out what a process is doing.

Remember to use the fork (`-f`)!

I didn't realize that snapd was forking a process for writing, and so it took
way more additional time to solve the issue, because I ran strace without the
fork option and snapd didn't appear to be doing anything (doh!)

I did run across a new tool in my toolbox of `blktrace` and `blkparse` which are
sort of like `strace` for block devices.
