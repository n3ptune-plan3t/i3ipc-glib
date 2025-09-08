# Maintainer: Your Name <your.email@example.com>
pkgname=i3ipc-glib
pkgver=1.0.1
pkgrel=1
pkgdesc="A C interface library to the i3 window manager"
arch=('x86_64')
url="https://github.com/altdesktop/i3ipc-glib"
license=('GPL3')
depends=('libglib2.0-0' 'libjson-glib-1.0-0' 'libxcb1')
makedepends=('build-essential' 'autotools-dev' 'libglib2.0-dev' 'libjson-glib-dev' 'gobject-introspection' 'libxcb1-dev' 'xcb-proto' 'gtk-doc-tools')
source=("$pkgname-$pkgver.tar.gz::$url/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  ./autogen.sh --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  make DESTDIR="$pkgdir/" install
}
