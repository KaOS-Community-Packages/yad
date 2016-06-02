pkgname=yad
pkgver=0.36.3
pkgrel=1
pkgdesc="A fork of zenity - display graphical dialogs from shell scripts or command line"
arch=('x86_64')
url="http://sourceforge.net/projects/yad-dialog"
license=('GPL3')
depends=('gtk3' 'hicolor-icon-theme')
makedepends=('intltool')
install="$pkgname.install"
source=("http://sourceforge.net/projects/${pkgname}-dialog/files/${pkgname}-${pkgver}.tar.xz")
sha512sums=('dca49f05ff1188fd34c0f9375cd305afee48e093aeb362f0359d29f3691cbd8f55dcb5bb2c9eec6f182b35349a9a52efe3197b5332f8a6f78536e807312d447d')

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
