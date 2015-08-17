# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Manuel Pelzel <issac007008@gmail.com>
pkgname='poomf'
pkgver='r76.12fed7da6a'
pkgrel=1
url="https://github.com/jschx/poomf"
pkgdesc='command-line uploader for pomf.se and uguu.se'
arch=('any')
license=('GPL')
depends=('curl' 'libnotify' 'maim' 'slop' 'xclip' 'xorg-xprop')
makedepends=('git')
source=("$pkgname::git+https://github.com/jschx/poomf.git")
md5sums=('SKIP')
pkgver() {
    cd $srcdir/poomf/
    printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}
package() {
	mkdir -p $pkgdir/usr/local/bin
	install $srcdir/poomf/poomf $pkgdir/usr/local/bin/poomf -m 755 || return 1
}
