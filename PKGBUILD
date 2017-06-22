# Maintainer: Joseph Kogut <joseph.kogut@gmail.com>

_gitname="meson_gx_mali_450"
pkgname=dkms-mali-utgard-meson
pkgver=r6p1_01rel0
pkgrel=1
pkgdesc="Mali Utgard Kernel Module for meson_drm (Linux 4.12+)"
arch=('aarch64')
url="https://github.com/jakogut/$_gitname"
license=('MIT')
install="$pkgname".install
depends=('linux>4.12' 'linux-headers>4.12' 'dkms')
makedepends=('git')
provides=('dkms-mali')
conflicts=('dkms-mali')
options=(!strip)
source=("git+${url}.git" "dkms.conf")

md5sums=('SKIP'
         '8a499af5f7faad49cede30c12ac7ffc5')

package() {
	cp dkms.conf "$srcdir/$_gitname/driver/src/devicedrv/mali"
	cd "$srcdir/$_gitname/driver/src/devicedrv/mali"
	mkdir -p "$pkgdir/usr/src/mali-utgard-meson-$pkgver"
	cp -r . "$pkgdir/usr/src/mali-utgard-meson-$pkgver"
}
