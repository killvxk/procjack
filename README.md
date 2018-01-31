# process-inject

Inject code into a running process.

## Example

This will inject a string into a running process 'dummy'.
```
$ cd src
$ make
$ ./dummy &
$ ./inject -p $(pidof dummy) -f ./count
```

Quick-n-dirty command to verify that a process is running multiple threads
```
$ ps -eLF | head -1; ps -eLF | grep -i dummy
```

## Dependencies

* [Capstone](http://www.capstone-engine.org/documentation.html) (`apt-get install libcapstone3 libcapstone-dev`)
