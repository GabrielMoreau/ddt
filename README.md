# SoftWare / DDT - Computer Names and IP Address Management (IPAM)

## Description

DDT is an acronym for DHCP-DNS-Tools.
In practise, DDT is an IP Address Management (IPAM) service.
It has been used in the LEGI laboratory for over 10 years.
```bashddt``` (```dhcp-dns-tools```) is a small tool to maintain a set of computers/IP.
In order to help you in this task, ddt command has a set of action
to generated DHCP and DNS configuration files.

The tool is quite effective and tries to keep things simple
but easily configurable for your site like a swiss army knife.
Everything is saved in a YAML database
and entries could be added, deleted, or modified by the command line.

All the command help and description is on the online manual
[https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/ddt/ ddt]

## Debian package

Debian is a GNU/Linux distribution.
Debian (and certainly Ubuntu) package for amd64 arch could be download on: https://legi.gricad-pages.univ-grenoble-alpes.fr/soft/trokata/ddt/download..

You can then install it with

```bash
sudo dpkg -i ddt_*_amd64.deb
```
(just replace * with the version you have donwloaded).


## Software repository

All code is under **free license**.
Scripts in `bash` are under GPL version 3 or later (http://www.gnu.org/licenses/gpl.html),
the `perl` scripts are under the same license as `perl` itself ie the double license GPL and Artistic License (http://dev.perl.org/licenses/artistic.html).

All sources are available on the campus forge: https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/ddt

The sources are managed via subversion (http://subversion.tigris.org/).
It is very easy to stay synchronized with these sources

 * initial recovery
```bash
git clone https://gricad-gitlab.univ-grenoble-alpes.fr/legi/soft/trokata/ddt
```
 * the updates thereafter
```bash
git pull
```

It is possible to have access to writing at the forge on reasoned request to [Gabriel Moreau](mailto:Gabriel.Moreau__AT__legi.grenoble-inp.fr).
For issues of administration time and security, the forge is not writable without permission.
For the issues of decentralization of the web, autonomy and non-allegiance to the ambient (and North American) centralism, we use our own forge...

You can propose an email patch of a particular file via the `diff` command.
Note that `svn` defaults to the unified format (`-u`).
Two examples:
```bash
diff -u ddt.org ddt.new > ddt.patch
svn diff ddt > ddt.patch
```
We apply the patch (after having read and read it again) via the command
```bash
patch -p0 < ddt.patch
```
