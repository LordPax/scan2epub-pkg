# Maintainer: teddy gauthier <teddy.gauthier@outlook.com>

pkgname=scan2epub
pkgver=1.3.0
pkgrel=1
pkgdesc="Download scan of manga and convert it to epub"
arch=(x86_64 i686 armv7h aarch64)
url="https://github.com/LordPax/go-${pkgname}"
license=(MIT)
depends=()
makedepends=(go)
source=("${url}/archive/refs/tags/v${pkgver}.tar.gz")
md5sums=('dd257aa1c0bd2d709eda26b8df461b27')

build() {
	cd "go-${pkgname}-${pkgver}"
	go mod download
	go build
}

package() {
	install -Dm755 "go-${pkgname}-${pkgver}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}
