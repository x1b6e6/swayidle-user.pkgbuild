# Maintainer: x1b6e6 <ftdabcde@gmail.com>

pkgname=swayidle-user
pkgver=1.0.4
pkgrel=1
pkgdesc="user scripts for swayidle"
arch=('any')
replaces=('swayidle-users')
conflicts=('swayidle-users')
depends=(
	"bash"
	"swayidle"
)

source=(
	"swayidle.sh"
	"swayidle.service"
	"swayidlecmd.sh"
)
sha1sums=('24c2aad6dea5d3ce13237393e9971eb39d66ed8e'
          '76b8bb1fd900b136ac752a306e215650f5e240ca'
          'e7ef73585fb0d27cf6b6d9b3ee79c7d9e3729324')

package() {
	cd "$srcdir"

	install -Dm755 "$srcdir/swayidle.sh" "$pkgdir/usr/lib/swayidle/swayidle-users"
	install -Dm755 "$srcdir/swayidlecmd.sh" "$pkgdir/usr/lib/swayidle/swayidle-cmd"
	install -Dm644 "$srcdir/swayidle.service" "$pkgdir/usr/lib/systemd/user/swayidle.service"
}
# vim: set ts=4 sw=0 noexpandtab autoindent :
