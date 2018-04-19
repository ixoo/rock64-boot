# Maintainer: Julien Etienne <julien.etienne@gmail.com>
pkgname=rock64-boot
pkgver=1
pkgrel=0
pkgdesc="Hook to update the boot image on the Rock64 board"
url="https://github.com/ixoo/rock64-boot"
depends=('linux-aarch64')
arch=('aarch64')
license=("Apache")
source=('boot_update.hook' 'boot_update')
md5sums=('d5073796fa69ca71e9bf6d920bf478dd'
         '35b5c4f8437530289cb724c19894c868')

package() {
	install -dm755 ${pkgdir}/etc/pacman.d/hooks/
	install -m 644 ${srcdir}/boot_update.hook ${pkgdir}/etc/pacman.d/hooks/boot_update.hook
	install -Dm755 ${srcdir}/boot_update ${pkgdir}/usr/bin/boot_update
}


