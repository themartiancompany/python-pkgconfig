# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgname=python-pkgconfig
pkgver=1.5.3
pkgrel=1
pkgdesc='Python module to interface with the pkg-config command line tool'
arch=(any)
url='https://github.com/matze/pkgconfig'
license=(MIT)
depends=(python)
makedepends=(python-setuptools)
source=(https://pypi.io/packages/source/p/pkgconfig/pkgconfig-$pkgver.tar.gz)
sha256sums=('41fb65d14fa918cedd7e205d95331162692dad2edee1441b485665b1f69a61c7')

package() {
  cd pkgconfig-$pkgver
  
  python setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
