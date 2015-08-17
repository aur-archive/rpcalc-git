# Maintainer: Quint Guvernator <quintus.public@gmail.com>
pkgname=rpcalc-git
pkgver=20130923
pkgrel=2
pkgdesc="A reverse polish notation calculator written in Python 3."
arch=('any')
url="http://qguv.github.io/rpcalc/"
license=('GPL3')
depends=('python>=3.3')
makedepends=('git')
conflicts=('rpcalc')
provides=('rpcalc')
source=("$pkgname"::git://github.com/qguv/rpcalc.git)
md5sums=('SKIP') # Because the sources are not static, skip Git checksum:

pkgver() {
  cd "$pkgname"
  local ver=$(git describe --always)
  printf "%s\n" "${ver//-/.}"
}

package() {
  cd "$pkgname"
  python setup.py install --root="$pkgdir/" --optimize=1
}

# vim:set ts=2 sw=2 et:

