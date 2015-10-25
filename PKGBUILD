pkgname=yad
pkgver=0.31.2
pkgrel=1
pkgdesc="A fork of zenity - display graphical dialogs from shell scripts or command line"
arch=('x86_64')
url="http://sourceforge.net/projects/yad-dialog"
license=('GPL3')
depends=('gtk3' 'hicolor-icon-theme')
makedepends=('intltool')
install="$pkgname.install"
source=("http://sourceforge.net/projects/${pkgname}-dialog/files/${pkgname}-${pkgver}.tar.xz")
sha512sums=('211c7ec5b4194849a1f9629dc86132600f55aaea3e5fc1c537f6fe14d5f7f103e8411ff81601561f5b95891256ba321c24065988901c4090fa033364b9a161c8')

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
