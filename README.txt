NAME
    check_freebsd_memory - Nagios plugin to report on FreeBSD memory usage

DESCRIPTION
    This script acts as a plugin module for the Nagios IT infrastructure
    monitoring system. It on a FreeBSD server to pull for memory information
    through sysctl(8). This plugin reports on the following 17 memory
    measurements:

    *   free_memory
    *   processes_in_run_queue
    *   processes_in_run_queue_on_disk_wait
    *   processes_in_run_queue_on_page_wait
    *   processes_in_run_queue_sleeping
    *   real_memory_active
    *   real_memory_total
    *   real_memory_usage
    *   shared_real_memory_active
    *   shared_real_memory_total
    *   shared_real_memory_usage
    *   shared_virtual_memory_active
    *   shared_virtual_memory_total
    *   shared_virtual_memory_usage
    *   virtual_memory_active
    *   virtual_memory_total
    *   virtual_memory_usage

    This has been tested with FreeBSD 7.1.

SYNOPSIS
  Command Line Interface
    Get the percentage of real memory that's currently in use:

            check_freebsd_memory -m real_memory_usage -w 80 -c 90

    Get the percentage of virtual memory that's currently in use:

            check_freebsd_memory -m virtual_memory_usage -w 80 -c 90

    Run this script with command line options stored in a configuration
    file:

            check_freebsd_memory --extra-opts=my_config.ini

SEE ALSO
    If using an external configuration file, it should be structured
    according to the specification at
    <http://nagiosplugins.org/extra-opts/>.

    Thresholds given to this script should be in the format specified at
    <http://nagiosplug.sourceforge.net/developer-guidelines.html>.

    This module is built upon Nagios::Plugin by the Nagios Plugin
    Development Team. Further reading on Nagios, NPRE, and Nagios Plugins is
    available at <http://nagios.com/>.

AUTHOR
    This script is written and maintained by Danne Stayskal
    <danne@stayskal.com> and is available on his website, at
    <http://danne.stayskal.com/software/check_frebsd/>.

LICENSE
    Copyright (C) 2009 by Danne Stayskal.

    This program is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License as published by the
    Free Software Foundation; either version 2 of the License, or (at your
    option) any later version.

    This program is distributed in the hope that it will be useful, but
    WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General
    Public License for more details.

    You should have received a copy of the GNU General Public License along
    with this program; if not, write to the Free Software Foundation, Inc.,
    59 Temple Place, Suite 330, Boston, MA 02111-1307 USA

    Nagios, the Nagios logo, and Nagios graphics are the servicemarks,
    trademarks, or registered trademarks owned by Nagios Enterprises. All
    other servicemarks and trademarks are the property of their respective
    owner.

