# Maintainer: lobotomius at gmail dot com

pkgname=lzwvl
pkgver=1
pkgrel=1
pkgdesc="c64 data compression software"
arch=('i686' 'x86_64')
url="http://csdb.dk/release/?id=81773"
license=('unknown')
source=('http://csdb.dk/getinternalfile.php/78272/source.rar' 'lzwvl.patch')
md5sums=('1248080a585e3c780f3345fe6994409d' 'b33be311de264e1966ab2b62799a8886')
build() {
    cd "$srcdir"
    patch -Np1 -i lzwvl.patch test.c
    gcc -o lzwvl test.c
}

package() {
    cd "$srcdir"
    mkdir -p "$pkgdir/usr/bin"
    install -m 755 lzwvl "$pkgdir/usr/bin"
}
