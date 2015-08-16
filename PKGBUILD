# Maintainer: Elie Bouttier <elie@bouttier.eu.org>
# Contributor: Pierre Carrier <pierre@gcarrier.fr>
_ghuser=freelan-developers
pkgname=libasiotap
pkgver=2.0
_pkgid=7cb2142
pkgrel=2
pkgdesc="A portable C++ TAP adapter extension for the Boost::ASIO library"
arch=(i686 x86_64)
url="http://www.freelan.org/"
license=('GPL')
depends=('boost-libs')
makedepends=('scons' 'freelan-buildtools' 'boost')
source=("https://github.com/$_ghuser/$pkgname/tarball/$pkgver")
md5sums=('c05e5c56ec7263f59f4c893231908630')

sconsflags="-j1"

build() {
  cd "$srcdir/$_ghuser-$pkgname-$_pkgid"
  scons $sconsflags
}

package() {
  cd "$srcdir/$_ghuser-$pkgname-$_pkgid"
  scons install $sconsflags prefix="$pkgdir/usr"
}
