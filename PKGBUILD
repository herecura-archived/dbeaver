# Maintainer: Arne Hoch <arne@derhoch.de>

pkgname=dbeaver
pkgver=4.0.8
pkgrel=1
pkgdesc="A free universal database tool for developers and database administrators"
arch=('i686' 'x86_64')
url="http://dbeaver.jkiss.org/"
license=("GPL2")
depends=('java-runtime>=1.8' 'gtk2' 'gtk-update-icon-cache')

source=('dbeaver.desktop')
source_i686=("http://dbeaver.jkiss.org/files/$pkgver/dbeaver-ce-$pkgver-linux.gtk.x86.tar.gz")
source_x86_64=("http://dbeaver.jkiss.org/files/$pkgver/dbeaver-ce-$pkgver-linux.gtk.x86_64.tar.gz")

sha256sums=('cf1e850dcb3544507eeb59b8d2e84b67cd25b546e3eaf03a0ab27ca841361478')
sha256sums_i686=('bb62c7db1d0f86309888389c9dc2e52c7362ddb52e48b6cf3d8fc496400b4ffe')
sha256sums_x86_64=('61a123c25ef87425adfabdbab0c9385c23dc407027c55ad538970efd82eec77a')

package() {
  cd "$pkgdir"
  mkdir -p opt/
  mkdir -p usr/bin
  mkdir -p usr/share/applications
  mkdir -p usr/share/icons/hicolor/48x48/apps
  
  cp -r "$srcdir/$pkgname" opt/
  cp opt/dbeaver/icon.xpm usr/share/icons/hicolor/48x48/apps/dbeaver.xpm
  chmod u=rwx,og=rx "$pkgdir/opt/dbeaver/dbeaver"
  ln -s /opt/dbeaver/dbeaver usr/bin/dbeaver
  install -m 644 "$srcdir/dbeaver.desktop" "$pkgdir/usr/share/applications/"
}

