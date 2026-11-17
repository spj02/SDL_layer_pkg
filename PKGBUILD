# Maintainer: Jonas S. <spj02@outlook.de>

pkgname=sdl3_layer
pkgver=1.0.1
pkgrel=1
pkgdesc='Wayland (wlroots) layer shell for SDL3'
arch=('x86_64')
url='https://github.com/spj02/SDL_layer'
license=('Zlib')
depends=('glibc' 'sdl3' 'wayland')
makedepends=('meson' 'sdl3' 'wayland')
source=("https://github.com/spj02/SDL_layer/archive/refs/tags/${pkgver}.tar.gz")
sha512sums=('3ba1e01cd7d24bcae9385d5d4163283d3133a5eccd265e62b03a1735a2a406d5378f83393010a950089fc710b7d00c7ba964cb0768d67f95952d2d4cfa3dba9f')

build() {
	arch-meson "SDL_layer-${pkgver}" build
  ninja -C build
}

package() {
	DESTDIR="${pkgdir}" ninja -C build install
}
