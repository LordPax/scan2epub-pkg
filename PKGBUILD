# Maintainer: teddy gauthier <teddy.gauthier@outlook.com>

pkgname=scan2epub
pkgver=1.2.0
pkgrel=1
pkgdesc="Download scan of manga and convert it to epub"
arch=('x86_64')
url="https://github.com/LordPax/go-${pkgname}"
license=('MIT')
depends=()
makedepends=('go')
source=("${url}/archive/refs/tags/v${pkgver}.tar.gz")
md5sums=('181dd06f5c403794ff9f415553d18d9c')

build() {
	cd "go-${pkgname}-${pkgver}"
	go mod download
	go build
}

package() {
	install -Dm755 "go-${pkgname}-${pkgver}/${pkgname}" "${pkgdir}/usr/bin/${pkgname}"
}
