# Maintainer: OmeGa <omega at mailoo dot org>

pkgname=nemo-seahorse-git
_gitname=nemo-extensions
pkgver=20130725
pkgrel=1
pkgdesc="An extension for Nemo which allows encryption and decryption of OpenPGP files using GnuPG."
arch=('i686' 'x86_64')
url="https://github.com/linuxmint/nemo-extensions"
license=('GPL2')
depends=('gconf' 'libcryptui' 'nemo')
makedepends=('intltool' 'git')
options=('!libtool')
install=$pkgname.install
source=('git://github.com/linuxmint/nemo-extensions.git')
sha1sums=('SKIP')

pkgver() {
  date -u +%Y%m%d
}

build() {
  cd "$srcdir/$_gitname/nemo-seahorse"

  ./configure \
    --prefix=/usr \
    --sysconfdir=/etc \
    --localstatedir=/var
  make
}

package() {
  cd "$srcdir/$_gitname/nemo-seahorse"
  make DESTDIR="$pkgdir" install
}

# vim:set ts=2 sw=2 et:
