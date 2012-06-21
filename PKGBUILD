# $Id$
# Maintainer: Sebastien Luttringer <seblu+arch@seblu.net>
# Contributor: Anton Bazhenov <anton.bazhenov at gmail>
# Contributor: Lone_Wolf <lonewolf@xs4all.nl>

pkgname=cfv
pkgver=1.18.3
pkgrel=4
pkgdesc='An utility to both test and create checksum files'
arch=('any')
url='http://cfv.sourceforge.net/'
license=('GPL')
depends=('python2')
optdepends=('bittorrent: for torrent checking')
source=("http://downloads.sourceforge.net/$pkgname/$pkgname-$pkgver.tar.gz")
md5sums=('1be9039c2ab859103d70b6c4f4e5edf5')

build() {
  cd $pkgname-$pkgver
  patch -p 0 << DIFF
--- cfv
+++ cfv
@@ -1,3 +1,3 @@
-#! /usr/bin/env python
+#! /usr/bin/env python2
 
 #    cfv - Command-line File Verify
DIFF
}

package() {
  make -C "$pkgname-$pkgver" install=install PYTHON=python2 prefix=/usr \
    mandir=/usr/share/man DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 ft=sh et:
