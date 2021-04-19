# Maintainer: Peter Eisenmann <p3732 at getgoogleoff dot me>
pkgname=triumphal-backgrounds
pkgver=2021.04.20
pkgrel=1
pkgdesc="Backgrounds for Triumphal"
arch=('any')
url="https://github.com/triumphal-arch/triumphal-backgrounds"
license=('GPL3')
depends=()
makedepends=('git' 'ninja' 'meson')
source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

build() {
	arch-meson $pkgname build
	meson compile -C build
}

package() {
	DESTDIR="$pkgdir" meson install -C build
}
