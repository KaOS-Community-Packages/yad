pkgname=yad
pkgver=0.31.3
pkgrel=1
pkgdesc="A fork of zenity - display graphical dialogs from shell scripts or command line"
arch=('x86_64')
url="http://sourceforge.net/projects/yad-dialog"
license=('GPL3')
depends=('gtk3' 'hicolor-icon-theme')
makedepends=('intltool')
install="$pkgname.install"
source=("http://sourceforge.net/projects/${pkgname}-dialog/files/${pkgname}-${pkgver}.tar.xz")
sha512sums=('fb0342f74e84efe6b457911f6a7fa5d6989518824004a07106863ec4bb719b50d9bb5bff90f21278581f9eafd68f91e90959b82d269ffab36915edcb3a83e355')

prepare() {
    cd "${srcdir}/${pkgname}-${pkgver}"
}

build() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    ./configure --prefix=/usr --with-gtk=gtk3 --enable-icon-browser --disable-html
    make
}

package() {
    cd "${srcdir}/${pkgname}-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
