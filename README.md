# Simple Shell :shell:

A simple UNIX command interpreter written as part of the low-level programming track at ALX.

## Description :speech_balloon:

**Simple Shell** is a simple UNIX command language interpreter that reads commands from either a file or standard input and executes them.

### Invocation :running:

Usage: **hsh** [filename]

To invoke **simple shell**, compile all `.c` files in the repository and run the resulting executable:

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o hsh
./hsh
```

**Simple shell** can be invoked both interactively and non-interactively. If **simple shell** is invoked with standard input not connected to a terminal, it reads and executes received commands in order.

Example:
```
$ echo "echo 'hello'" | ./hsh
'hello'
$
```

If **simple shell** is invoked with standard input connected to a terminal (determined by [isatty](https://linux.die.net/man/3/isatty)(3)), an *interactive* shell is opened. When executing interactively, **simple shell** displays the prompt `$ ` when it is ready to read a command.

Example:
```
$./hsh
$
```

Alternatively, if command line arguments are supplied upon invocation, **simple shell** treats the first argument as a file from which to read commands. The supplied file should contain one command per line. **Simple shell** runs each of the commands contained in the file in order before exiting.

Example:
```
$ cat test
echo 'hello'
$ ./hsh test
'hello'
$
```
## Authors :black_nib:

* Dinton Harold Ainemukama<[dintonharold87](https://github.com/dintonharold87)>
* Donald Ainebyona <[DonAine](https://github.com/DonAine)>
