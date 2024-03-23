# SPDX-License-Identifier: AGPL-3.0
# 
# Maintainer:  Pellegrino Prevete <cGVsbGVncmlub3ByZXZldGVAZ21haWwuY29tCg== | base -d>
# Maintainer:  Truocolo <truocolo@aol.com>
# Maintainer: Antonio Rojas <arojas@archlinux.org>

_py="python"
_pkg="pkgconfig"
pkgname="${_py}-${_pkg}"
pkgver=1.5.5
pkgrel=5
pkgdesc='Python module to interface with the pkg-config command line tool'
arch=(
  any
)
url='https://github.com/matze/pkgconfig'
license=(
  MIT
)
depends=(
  "${_py}"
)
makedepends=(
  "${_py}-setuptools"
)
_pypi="https://pypi.io/packages/source"
source=(
  "${_pypi}/${_pkg::1}/${_pkg}/${_pkg}-${pkgver}.tar.gz"
)
sha256sums=(
  'deb4163ef11f75b520d822d9505c1f462761b4309b1bb713d08689759ea8b899')

package() {
  cd \
    "${_pkg}-${pkgver}"
  "${_py}" \
    setup.py \
      install \
        --prefix=/usr \
        --root "${pkgdir}" \
        --optimize=1
  install \
    -Dm644 \
    LICENSE \
    "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

# vim:set sw=2 sts=-1 et:
