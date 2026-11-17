# Maintainer: Jonas S. <spj02@outlook.de>

pkgname=sdl3_layer
pkgver=1.0.0
pkgrel=1
pkgdesc='Wayland (wlroots) layer shell for SDL3'
arch=('x86_64')
url='https://github.com/spj02/SDL_layer'
license=('Zlib')
depends=('glibc' 'sdl3' 'wayland')
makedepends=('meson')
source=("https://github.com/spj02/SDL_layer/archive/refs/tags/${pkgver}.tar.gz")
sha512sums=('2494707ae727831f2d566e4d8bae0460b5f0912e386bfb5e28030bd19c13cfdc393da851aad034179a6636d9a0262c38eda57656cf3ed629226cb899644babf9')

build() {
	arch-meson "SDL_layer-${pkgver}" build
  ninja -C build
}

package() {
	DESTDIR="${pkgdir}" ninja -C build install
}
