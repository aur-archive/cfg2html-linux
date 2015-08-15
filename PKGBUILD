#maintainer aking9 <arking@gmail.com>
pkgname=cfg2html-linux
pkgver=2.42
pkgrel=1
pkgdesc='Cfg2html is a UNIX shell script similar to getsysinfo or get_config, except that it creates a HTML (and plain ASCII) system documentation for HP-UX 10.xx/11.xx, Integrity Virtual Machine, SCO-UNIX, AIX, Sun OS and Linux systems. Plug-ins for SAP, Oracle, Informix, Serviceguard, Fiber Channel/SAN, TIP/ix, OpenText (IXOS/LEA), SAN Mass Storage like MAS, EMC, EVA, XPs, Network Node Manager and DataProtector etc. are included. The first versions of cfg2html were written for HP-UX. Meanwhile the cfg2html HP-UX stream was ported to all major *NIX platforms and small embedded systems.

Some consider it to be the Swiss army knife for the Account Support Engineer, Customer Engineer, Systemadmin, Solution Architect etc. Originally developed to plan a system update, it was also found useful to perform basic troubleshooting or performance analysis. The production of nice HTML and plain ASCII documentation is part of its utility. '
arch=('any')
url="http://www.cfg2html.com"
license=('unknown')
depends=('setserial')
source="http://www.cfg2html.com/cfg2html-linux-$pkgver-20100319_all.zip"
source="http://www.cfg2html.com/cfg2html-linux-$pkgver-20120220_all.zip"
md5sums=('1195aac0407b7eeebd03fbeb498b884f')

build () {
         cd "$startdir/src"
         
         # Because of the way the cfg2html source is distributed (through a yahoo group
         # and as the zip file above) a second extraction is needed.
         tar xvf cfg2html-linux_$pkgver-1.tar.gz
         
         cd "cfg2html-linux-$pkgver"  
                        
         install -d "$startdir/pkg/usr/bin"
         install -d "$startdir/pkg/etc/cfg2html"
         install -d "$startdir/pkg/usr/share/man/man8"
         install cfg2html-linux "$startdir/pkg/usr/bin"  
         install cfg2html "$startdir/pkg/usr/bin"
         install cfg2html-linux.8 "$startdir/pkg/usr/share/man/man8"
         install -m 644 files "$startdir/pkg/etc/cfg2html"
         install -m 644 systeminfo "$startdir/pkg/etc/cfg2html"
         install -m 644 plugins "$startdir/pkg/etc/cfg2html"
}

