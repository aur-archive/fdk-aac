# Maintainer: DrZaius <lou[at]fakeoutdoorsman[dot]com>

pkgname=fdk-aac
pkgver=0.1.1
pkgrel=2
pkgdesc="Fraunhofer FDK AAC codec library"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/opencore-amr/"
license=('custom')
depends=('glibc')
options=('!emptydirs' '!libtool')
source=(http://downloads.sourceforge.net/opencore-amr/${pkgname}-${pkgver}.tar.gz)
md5sums=('87ed9dd60e933b5cb4fe72bdc749480e')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package () {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  install -Dm644 NOTICE "${pkgdir}/usr/share/licenses/${pkgname}/NOTICE"
}
