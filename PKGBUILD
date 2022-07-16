# Maintainer: funinkina

pkgname=('manjaro-minimal-bootsplash')
pkgver=0.1
pkgrel=1
url="https://github.com/funinkina/manjaro-minimal-bootsplash"
arch=('x86_64')
pkgdesc="Minimal bootsplash theme for Manjaro linux."
license=('GPL')
depends=()
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-minimal.sh'
	'bootsplash-minimal.initcpio_install'
	'spinner.gif'
	'logo.png')

sha256sums=('51559d3ccfb448b03fa6439faf5869dbd0c2fbda1b5d5bf5d4ba70e60937472a'
            '5f4d360f6cf2f27abc4692310f731237af09a3597a725fae7254d6f51990aa68'
            '9f1fdaf68364ed14398494d4092ed4922ea31dcd1818400b181fcbdb358c9514'
            '880413c22681904c649848e96f043c0a1cd691604c77f1374cfee488a4c33ab4'
            '2bba62075bbfd8618077c159761fc9c5a0579f3010ff9349145874b449cfb35e')

build() {
  cd "$srcdir"
  sh ./bootsplash-minimal.sh
}

package_manjaro-minimal-bootsplash() {
  pkgdesc="Bootsplash Theme 'minimal'"
  cd "$srcdir"

  install -Dm644 "$srcdir/manjaro-minimal-bootsplash" "$pkgdir/usr/lib/firmware/bootsplash-themes/minimal/bootsplash"
  install -Dm644 "$srcdir/manjaro-bootsplash-minimal.initcpio_install" "$pkgdir/usr/lib/initcpio/install/manjaro-minimal-bootsplash"
}
