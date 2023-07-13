# Maintainer: Daniel Milenov, Mario Sánchez <ghfetch.contact@gmail.com>
pkgname='ghfetch'
pkgver='1.2.0'
pkgrel=1
pkgdesc="A nice way to display CLI Github user / repo / organization info inspired in neofetch "
arch=('x86_64')
url="https://github.com/ghfetch/ghfetch"
license=('MIT')
depends=('python' 'python-aiohttp' 'python-requests'  'python-pillow' 'python-rich')
makedepends=('git')
source=('ghfetch::https://github.com/ghfetch/ghfetch.git')
md5sums=('SKIP')

build() {
    cd "../../$pkgname"
    python setup.py build
}

package() {
    cd "../../$pkgname"
    install -Dm755 ./ghfetch "$pkgdir/usr/bin/$pkgname"
    install -Dm644 ./README.md "$pkgdir/usr/share/doc/$pkgname"
}