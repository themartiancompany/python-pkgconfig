# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgbase=python-pkgconfig
pkgname=(python2-pkgconfig python-pkgconfig)
pkgver=1.4.0
pkgrel=1
pkgdesc="Python module to interface with the pkg-config command line tool"
arch=(any)
url="https://github.com/matze/pkgconfig"
license=(MIT)
makedepends=(python-setuptools python2-setuptools)
source=($pkgbase-$pkgver.tar.gz::"https://github.com/matze/pkgconfig/archive/v$pkgver.tar.gz")
sha256sums=('38c5de8392f4acfe7f36b25d113c496d68f534e983afdbd0ba7240c8c475b161')

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
