pkgname=libslirp
pkgver=4.8.0
pkgrel=1
pkgdesc='A user-mode networking library used by virtual machines, containers or various tools'
arch=('x86_64')
url='https://gitlab.freedesktop.org/slirp/libslirp'
license=('BSD-3-Clause')
depends=('glib2')
makedepends=('meson' 'git')
source=("git+https://gitlab.freedesktop.org/slirp/libslirp.git#tag=v${pkgver}")
sha512sums=('SKIP')
src_name='libslirp'

build() {
    cd "${src_name}"
    meson setup build --prefix=/usr
    cd build
    meson compile
}

package() {
    install -Dm644 ../LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
    cd "${src_name}/build"
    DESTDIR=${pkgdir} meson install
}
