pkgname=yad
pkgver=0.35.0
pkgrel=1
pkgdesc="A fork of zenity - display graphical dialogs from shell scripts or command line"
arch=('x86_64')
url="http://sourceforge.net/projects/yad-dialog"
license=('GPL3')
depends=('gtk3' 'hicolor-icon-theme')
makedepends=('intltool')
install="$pkgname.install"
source=("http://sourceforge.net/projects/${pkgname}-dialog/files/${pkgname}-${pkgver}.tar.xz")
sha512sums=('e82ac38d66c5ea2b9920bc7ae753059ce63b6b51f028532623058b929668a7f7b674983fdf6a2aa8ca256808406804c143dd143982aedad37d6b3a3268eb49d0')

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
