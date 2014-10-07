Description
================

This script takes manage postfix queues. You could search pattern, delete match result, list all queues and count messages group by subject. 

**WARNING**: Use this script at your own risk. When you delete queue, the email asociated is erased from disk, so you can not reverse the process. You must be superuser to use this script, if you don't, it will fail.



Installation
============

Checkout the script:

```bash
$ wget --no-check-certificate -O /usr/local/sbin/pfqueues https://raw.githubusercontent.com/cperezcerrato/pfqueues/master/pfqueues
```

Set permissions:
```bash
$ chmod +750 /usr/local/sbin/pfqueues
```

Feel free to place the script in any path you want.

Usage
=====

```bash
$ pfqueues -h
pfqueues [-h] [-l] [-c] [-v QUEUEID] [-p PATTERN] [-d]
    -h        Display this message.
    -l        List summary from all queues.
    -c        Count all messages group by subject.
    -p        Specify the pattern to search for.
    -d        Actually remove files not yank them, no -p will delete all the messages!
    -q        Quiet. Does not display individual queues when search pattern. Faster.
```


License and Author
==================
Copyright (C) May, 2014 Carlos Perez Cerrato <cperezcerrato@gmail.com>

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0
Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
