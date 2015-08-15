# Modified from original gmpc pkgbuild created by tobias <tobias@archlinux.org>
# Contributor: Lukas Miczka <lukascpu@gmail.com>

pkgname=gmpc-alarm
pkgver=11.8.16
pkgrel=2
pkgdesc="This plugin can start/stop/pause your music at a preset time."
arch=(i686 x86_64)
url="http://sarine.nl/gmpc/"
license="GPL"
depends=("libmpd>=${pkgver}" "gmpc>=${pkgver}" "libxml2" "intltool>=0.21")
source=(http://download.sarine.nl/Programs/gmpc/${pkgver}/${pkgname}-${pkgver}.tar.gz)
sha1sums=('5accff4dc60c30d5b0b29bf9c321c95b5432a17b')

build() {
  cd ${startdir}/src
  tar xzf ${pkgname}-${pkgver}.tar.gz 
  cd $startdir/src/$pkgname-$pkgver
  ./configure --prefix=/usr
  make || return 1
  make DESTDIR=$pkgdir install
}

