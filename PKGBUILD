# Maintainer: Germán Osella Massa <gosella@gmail.com>
# Based on a previous PKGBUILD available on AURv3.
# Contributor: Mariusz Libera <mariusz.libera@gmail.com>
# Contributor: Tianjiao Yin <ytj000@gmail.com>
# Contributor: Vinicius de Avila Jorge <vinicius.avila.jorge@gmail.com>
pkgname=cppreference
pkgver=20161029
pkgrel=1
pkgdesc="A complete reference for the features in the C++ Standard Library. HTML book."
arch=('any')
url="http://en.cppreference.com/"
license=('CCPL:cc-by-sa')
options=('!strip' '!emptydirs')
depends=('ttf-dejavu')
source=("http://upload.cppreference.com/mwiki/images/4/4c/html_book_20161029.tar.gz")
sha256sums=('ea830dd6e12a9278a26a383f11ee1ebd7d898c4c8bbfd1da6ad2311d201da1c8')

package() {
    rm "$srcdir/reference/common/DejaVuSansMonoCondensed60.ttf"
    rm "$srcdir/reference/common/DejaVuSansMonoCondensed75.ttf"
    mkdir -p "$pkgdir/usr/share/doc/cppreference"
    mv -t "$pkgdir/usr/share/doc/cppreference/" $srcdir/reference/*
}
