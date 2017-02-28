# Maintainer: Arne Hoch <arne@derhoch.de>

pkgname=dbeaver
pkgver=4.0.1
pkgrel=2
pkgdesc="A free universal database tool for developers and database administrators"
arch=('i686' 'x86_64')
url="http://dbeaver.jkiss.org/"
license=("GPL2")
depends=('java-runtime>=1.7' 'gtk2' 'gtk-update-icon-cache')

source=('dbeaver.desktop')
source_i686=("http://dbeaver.jkiss.org/files/$pkgver/dbeaver-ce-$pkgver-linux.gtk.x86.tar.gz")
source_x86_64=("http://dbeaver.jkiss.org/files/$pkgver/dbeaver-ce-$pkgver-linux.gtk.x86_64.tar.gz")

sha256sums=('cf1e850dcb3544507eeb59b8d2e84b67cd25b546e3eaf03a0ab27ca841361478')
sha256sums_i686=('7460cd6a32735d44eabda2db13bc8a7e62e2cdaf4a176286a5942431be275b23')
sha256sums_x86_64=('4960d0d2daf488eb74e0ca9fad40d7f737f4f2a3929b838e3eaedf4326792e6c')

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

