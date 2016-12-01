# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgbase=python-pkgconfig
pkgname=(python2-pkgconfig python-pkgconfig)
pkgver=1.2.1
pkgrel=1
pkgdesc="Python module to interface with the pkg-config command line tool"
arch=(any)
url="https://github.com/matze/pkgconfig"
license=(MIT)
makedepends=(python-setuptools python2-setuptools)
source=("https://github.com/matze/pkgconfig/archive/v$pkgver.tar.gz")
md5sums=('1c9d7c2e893a834793b8394a891f9de6')

package_python2-pkgconfig() {
  depends=(python2)
  cd pkgconfig-$pkgver

  python2 setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}

package_python-pkgconfig() {
  depends=(python)
  cd pkgconfig-$pkgver
  
  python setup.py install --prefix=/usr --root="$pkgdir" --optimize=1
  install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
