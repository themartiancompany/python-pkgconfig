# Maintainer: Antonio Rojas <arojas@archlinux.org>

pkgbase=python-pkgconfig
pkgname=(python2-pkgconfig python-pkgconfig)
pkgver=1.3.1
pkgrel=2
pkgdesc="Python module to interface with the pkg-config command line tool"
arch=(any)
url="https://github.com/matze/pkgconfig"
license=(MIT)
makedepends=(python-setuptools python2-setuptools)
source=($pkgbase-$pkgver.tar.gz::"https://github.com/matze/pkgconfig/archive/v$pkgver.tar.gz")
sha256sums=('b4b8277cf33df2bfdd73da2bc4faab1b4b65b6d12e295aa6c70987642bcfb5c7')

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
