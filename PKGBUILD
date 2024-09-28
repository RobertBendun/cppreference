# Maintainer: Robert Bendun <robert@bendun.cc>
# Based on a previous PKGBUILD available on AURv3.
# Contributor: Germán Osella Massa <gosella@gmail.com>
# Contributor: Mariusz Libera <mariusz.libera@gmail.com>
# Contributor: Tianjiao Yin <ytj000@gmail.com>
# Contributor: Vinicius de Avila Jorge <vinicius.avila.jorge@gmail.com>
pkgname=cppreference
pkgver=20240610
pkgrel=1
pkgdesc="A complete reference for the features in the C++ Standard Library. HTML Book"
arch=('any')
url="http://en.cppreference.com/"
license=('CCPL:cc-by-sa')
options=('!strip' '!emptydirs')
depends=('ttf-dejavu')
source=("https://github.com/PeterFeicht/cppreference-doc/releases/download/v20240610/html-book-20240610.tar.xz")
sha256sums=('bc2412a5eaf7f6094d4eb70f765bdf8f649e654a8aabf20160c5a81697684761')

package() {
	rm "$srcdir/reference/common/DejaVuSansMonoCondensed60.ttf"
	rm "$srcdir/reference/common/DejaVuSansMonoCondensed75.ttf"
	mkdir -p "$pkgdir/usr/share/doc/cppreference/html/"
	mv -t "$pkgdir/usr/share/doc/cppreference/html/" $srcdir/reference/*
	find "$pkgdir"/usr/share/doc/cppreference/html/ -type f -exec chmod 0644 {} \;
	find "$pkgdir"/usr/share/doc/cppreference/html/ -type d -exec chmod 0755 {} \;
}
