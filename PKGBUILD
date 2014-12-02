_pkgname=urlmatch
pkgname=lib${_pkgname}
pkgver=222
pkgrel=1
pkgdesc='A fast URL matcher library'
arch=('x86_64')
url="https://github.com/clbr/${_pkgname}"
license=('GPLv3')
makedepends=('git')
source=("git://github.com/clbr/${_pkgname}")
md5sums=('SKIP')

pkgver() {
	cd "${srcdir}/${_pkgname}"
	git rev-list --count HEAD
}

build() {
	cd "${srcdir}/${_pkgname}"
	make
}

package() {
	cd "${srcdir}/${_pkgname}"
	make install DESTDIR="${pkgdir}"
}
