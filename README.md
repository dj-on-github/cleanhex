# cleanhex
Cleans up hex files by removing 0x, non hex characters, whitespace and lines starting with #.

```
$ cleanhex -h
Usage: cleanhex [options] [filename]

Options:
  -h, --help            show this help message and exit
  -o FILE, --output=FILE
                        Write output to <filename> instead of stdout
  -v, --verbose         Show many internal gory details
```

For example..

```
$ cat dirtyhex.hex
# Some logged data
55DD76FD
0xA02E1933

9B,0x79, 0xC4, 0xDF
34 02 B3 60
477F 64BD

# more logged data
E89512 22
B5620xA944
433FC6B1
A5896DC7
70671810

$ cleanhex dirtyhex.hex
55DD76FD
A02E1933
9B79C4DF
3402B360
477F64BD
E8951222
B562A944
433FC6B1
A5896DC7
70671810
```

