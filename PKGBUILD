pkgname=fcitx5-table-ucxaf
pkgver=5.0.10
pkgrel=1
pkgdesc="UCxAf tables for Fcitx5"
arch=('any')
url="https://github.com/cosmo-arsh/fcitx5-table-ucxaf"
license=('GPL')
depends=('fcitx5-chinese-addons')
makedepends=('extra-cmake-modules' 'boost')

source=("fcitx5-table-ucxaf::git+https://github.com/cosmo-arsh/fcitx5-table-ucxaf.git")

sha512sums=('SKIP')


build(){
  cd $pkgname

  cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_INSTALL_LIBDIR=/usr/lib .
  make
}

package() {
  cd $pkgname
  make DESTDIR="$pkgdir" install
}