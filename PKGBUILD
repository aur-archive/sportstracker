# Maintainer: Dmitry Korzhevin <dkorzhevin at gmail dot com>

pkgname=sportstracker
pkgver=5.7.0
pkgrel=1
pkgdesc="Application for people which want to record their sporting activities"
arch=('any')
url="http://www.saring.de/sportstracker/"
license=('GPL')
depends=('java-environment')
source=(http://downloads.sourceforge.net/sportstracker/SportsTracker-$pkgver-bin.zip
        sportstracker.sh
        sportstracker.desktop)
md5sums=('d4a48b8dcfafa14da5eec20026bbf1ae'
         'e2dbfcde567a789dd2ce5ee372ed9a70'
         'f1bae50553e3afec0dd9a536d4445832')
build() {
  cd $srcdir/SportsTracker-$pkgver-bin

  install -D -m644 sportstracker-$pkgver.jar $pkgdir/usr/share/java/sportstracker/sportstracker-$pkgver.jar
  install -m644 lib/*.jar $pkgdir/usr/share/java/sportstracker

  install -D -m755 $srcdir/sportstracker.sh $pkgdir/usr/bin/sportstracker

  install -D -m644 $srcdir/sportstracker.desktop $pkgdir/usr/share/applications/sportstracker.desktop
  install -D -m644 st-logo-512.png $pkgdir/usr/share/pixmaps/sportstracker.png
}
