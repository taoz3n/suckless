# local pkgbuild
# Maintainer: crian <crian84@gmail.com>

pkgname=surf-crian-git
pkgver=2.0
pkgrel=1
pkgdesc='A simple Web browser based on WebKit/GTK+'
arch=('x86_64')
license=('MIT')
depends=('webkit2gtk' 'xorg-xprop')
conflicts=('surf')
provides=('surf')

build() {
    cd ..
    make
}

package() {
    cd ..
    make PREFIX=/usr DESTDIR="$pkgdir" install
    install -m644 -D LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
