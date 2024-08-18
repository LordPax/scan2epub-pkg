# Maintainer: teddy gauthier <teddy.gauthier@outlook.com>

pkgname=scan2epub
pkgver=1.4.0
pkgrel=1
pkgdesc="Download scan of manga and convert it to epub"
arch=(x86_64 i686 armv7h aarch64)
url="https://github.com/LordPax/go-${pkgname}"
license=(MIT)
depends=()
makedepends=(go)
source=("${url}/archive/refs/tags/v${pkgver}.tar.gz")
md5sums=('e55f2110f9223e90ec4b4220b9201969')

build() {
	cd "go-${pkgname}-${pkgver}"
	go mod download
	go build
}

package() {
	install -Dm755 "go-${pkgname}-${pkgver}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}
