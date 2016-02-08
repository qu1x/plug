> This file is part of Plug, see <https://qu1x.org/plug>.
> 
> Copyright (c) 2016 Rouven Spreckels <n3vu0r@qu1x.org>
> 
> Plug is free software: you can redistribute it and/or modify
> it under the terms of the GNU Affero General Public License version 3
> as published by the Free Software Foundation on 19 November 2007.
> 
> Plug is distributed in the hope that it will be useful,
> but WITHOUT ANY WARRANTY; without even the implied warranty of
> MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
> GNU Affero General Public License for more details.
> 
> You should have received a copy of the GNU Affero General Public License
> along with Plug. If not, see <https://www.gnu.org/licenses>.

Plug
====

Invoke command as soon as its device is plugged in.

Installation
============

Either getting a release
------------------------

1. Download stable source distribution tarball.

		wget https://qu1x.org/file/plug-1.0.0.tar.xz

2. Extract and enter.

		tar -xJf plug-1.0.0.tar.xz
		cd plug-1.0.0

Or getting a snapshot
---------------------

1. Clone repository.

		git clone https://github.com/qu1x/plug.git

2. Enter and generate latest source distribution.

		cd plug
		autoreconf -i

Installing one of them
----------------------

3. Configure, build, and install.

		./configure --sysconfdir=/etc
		make
		sudo make install

4. Keep to uninstall someday.

		sudo make uninstall

Usage
=====

* `plug [<CMD> [ARG]... <DEV>]`

Wait for `DEV` to be plugged in before invoking `<CMD> [ARG]... <DEV>`.
Without arguments, print help information.

* `plug picocom -b 115200 -- /dev/ttyUSB0`

Wait for USB-to-Serial adapter to be populated before invoking
dumb-terminal emulator with given baud rate to for example not miss
early debug messages of a booting device having just appeared.


Version
=======

plug-1.0.0 <https://qu1x.org/plug>

License
=======

GNU Affero General Public License version 3

Authors
=======

* Copyright (c) 2016 Rouven Spreckels <n3vu0r@qu1x.org>

