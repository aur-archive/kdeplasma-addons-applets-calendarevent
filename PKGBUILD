# Maintainer: t3ddy  <t3ddy1988 "at" gmail {dot} com>

pkgname=kdeplasma-addons-applets-calendarevent
pkgver=0.2
pkgrel=1
pkgdesc="A plasmoid displaying the days of the calendar in one column."
arch=('i686' 'x86_64')
url="http://kde-look.org/content/show.php/CalendarEvent?content=148928"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('gcc' 'cmake' 'automoc4')
source=("http://kde-look.org/CONTENT/content-files/148928-calendarevent-${pkgver}.tar.gz")
md5sums=('cf5a89f73ad68fb1f828904cca727b2d')

build() {
  cd "$srcdir/calendarevent"

  mkdir build && cd build

  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..

  make
}

package() {
  cd "$srcdir/calendarevent/build"

  make DESTDIR="$pkgdir/" install
}