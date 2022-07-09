pkgname=('lgwebosremote-git')
pkgver=r142.c38785d
pkgrel=1
pkgdesc="Command line webOS remote for LGTVs"
arch=('x86_64')
url="https://github.com/JonnyKreng/LGWebOSRemote"
license=('MIT')
depends=('python-wakeonlan' 'python-ws4py' 'python-requests' 'python-getmac')
makedepends=('git' 'python-setuptools')
source=("${pkgname%-*}::git+https://github.com/JonnyKreng/LGWebOSRemote.git")
provides=("lgtv")
conflicts=("lgtv")

md5sums=('SKIP')

pkgver() {
  cd "${pkgname%-*}"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "${pkgname%-*}"
  python setup.py install --root="${pkgdir}" --optimize=1
}
