pkgname=i3ipc-glib
pkgver=1.0.1
pkgrel=1
pkgdesc="A C interface library to i3wm"
arch=('x86_64')
url="https://github.com/altdesktop/i3ipc-glib"
license=('GPL3')
depends=('libxcb' 'glib2' 'json-glib')
makedepends=('autoconf' 'automake' 'libtool' 'pkg-config' 'gtk-doc-tools' 'gobject-introspection')
source=("git+https://github.com/altdesktop/i3ipc-glib.git#tag=v$pkgver")
sha256sums=('SKIP')

build() {
  cd "$srcdir/$pkgname"
  ./autogen.sh --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" install
}
