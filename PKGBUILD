pkgname=cfv
pkgver=1.17
pkgrel=1
pkgdesc="Verify  file consistency[sfv,csv,crc,md5,md5sum,torrent,par,par2 files]"
depends=('python')
url="http://cfv.sourceforge.net/"
source=(http://cesnet.dl.sourceforge.net/sourceforge/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('e8b627784acb613b4f49445973b3594d')

build() {
  cd $startdir/src/$pkgname-$pkgver

  mkdir -p $startdir/pkg/usr/{man/man1,bin}
  install -c -m 0644 cfv.1 $startdir/pkg/usr/man/man1/cfv.1
  install -c -m 0755 cfv $startdir/pkg/usr/bin/cfv
}
