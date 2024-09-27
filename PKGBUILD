# Maintainer: Robert Bendun <robert@bendun.cc>
# Based on a previous PKGBUILD available on AURv3.
# Contributor: Germán Osella Massa <gosella@gmail.com>
# Contributor: Mariusz Libera <mariusz.libera@gmail.com>
# Contributor: Tianjiao Yin <ytj000@gmail.com>
# Contributor: Vinicius de Avila Jorge <vinicius.avila.jorge@gmail.com>
pkgname=cppreference
pkgver=20240610
pkgrel=1
pkgdesc="A complete reference for the features in the C++ Standard Library."
arch=('any')
url="http://en.cppreference.com/"
license=('CCPL:cc-by-sa')
options=('!strip' '!emptydirs')
depends=('ttf-dejavu')
source=("https://github.com/PeterFeicht/cppreference-doc/releases/download/v20240610/cppreference-doc-20240610.tar.xz")
sha256sums=('840e08db99650fc58ea9fd0838e5141f2da4fa9f86968367b1549b06f54f5f26')

package() {
	rm "$srcdir/reference/common/DejaVuSansMonoCondensed60.ttf"
	rm "$srcdir/reference/common/DejaVuSansMonoCondensed75.ttf"
	mkdir -p "$pkgdir/usr/share/doc/cppreference/html/"
	mv -t "$pkgdir/usr/share/doc/cppreference/html/" $srcdir/reference/*
	find "$pkgdir"/usr/share/doc/cppreference/html/ -type f -exec chmod 0644 {} \;
	find "$pkgdir"/usr/share/doc/cppreference/html/ -type d -exec chmod 0755 {} \;
}
