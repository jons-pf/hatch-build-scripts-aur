# Maintainer: Jonathan Schilling <jons@proximafusion.com>
pkgname=hatch-build-scripts
pkgver=0.0.4
pkgrel=1
pkgdesc="A plugin for Hatch that runs build scripts and saves their artifacts."
arch=('any')
url="https://github.com/rmorshea/hatch-build-scripts"
license=('MIT')
makedepends=('git' 'python-build' 'python-installer')
depends=('python-pathspec' 'python-hatchling')
conflicts=(hatch-build-scripts)

source=("https://github.com/rmorshea/hatch-build-scripts/archive/refs/tags/v0.0.4.tar.gz")
sha256sums=('ab36bb473e724dda815a00f4d48c60b11a608c59c91f316042880c1f61fb9a1a')

build() {
	cd "$pkgname-$pkgver"
	python -m build -nw
}

package() {
	cd "$pkgname-$pkgver"
	python -m installer --destdir="$pkgdir" dist/*.whl
}
