# $Id$
# Maintainer: Gaetan Bisson <bisson@archlinux.org>

pkgname=xournal
pkgver=0.4.8.2016
pkgrel=1
pkgdesc='Notetaking and sketching application'
url='http://xournal.sourceforge.net/'
license=('GPL')
arch=('i686' 'x86_64')
optdepends=('ghostscript: import PS/PDF files as bitmap backgrounds')
depends=('libgnomecanvas' 'poppler-glib' 'shared-mime-info' 'desktop-file-utils' 'hicolor-icon-theme')
#source=("http://downloads.sourceforge.net/${pkgname}/${pkgname}-${pkgver}.tar.gz")
#sha256sums=('b25898dbd7a149507f37a16769202d69fbebd4a000d766923bbd32c5c7462826')

build() {
#	cd "${srcdir}/${pkgname}-${pkgver}"
  cd ..
  ./autogen.sh
	./configure --prefix=/usr
	make
}

package() {
#	cd "${srcdir}/${pkgname}-${pkgver}"
  cd ..
	make DESTDIR="${pkgdir}" install desktop-install
}