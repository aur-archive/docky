# Maintainer: György Balló <ballogy@freestart.hu>
# Contributor:  Jan "heftig" Steffens <jan.steffens@gmail.com>
# Contributor: dieghen89 <dieghen89@gmail.com>
# Contributor: Alessio 'Bl@ster' Biancalana <dottorblaster@gmail.com>

pkgname=docky
pkgver=2.1.3
pkgrel=4
pkgdesc="The finest dock no money can buy!"
url="http://wiki.go-docky.com/"
arch=('any')
license=('GPL')
depends=('gconf-sharp' 'libgnome-desktop-sharp' 'gnome-keyring-sharp' 'mono-addins' 'notify-sharp' 'rsvg2-sharp' 'wnck-sharp' 'hicolor-icon-theme' 'xdg-utils')
makedepends=('intltool' 'libgnome-sharp' 'gio-sharp')
install=$pkgname.install
source=("http://launchpad.net/$pkgname/2.1/$pkgver/+download/$pkgname-$pkgver.tar.gz")
md5sums=('7a40c25dff6b71c346e7791533f05b5f')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr --sysconfdir=/etc \
              --disable-schemas-install \
              --with-gconf-schema-file-dir=/usr/share/gconf/schemas
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir" install
}
