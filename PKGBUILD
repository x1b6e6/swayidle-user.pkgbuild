# Maintainer: x1b6e6 <ftdabcde@gmail.com>

pkgname=swayidle-users
pkgver=1.0.0
pkgrel=1
pkgdesc="user scripts for swayidle"
arch=('any')
depends=(
	"bash"
	"swayidle"
)

source=(
	"swayidle.sh"
	"swayidle.service"
)
sha1sums=('64a1edc68beeaaa29847f0b550051e12fb2bebb6'
          '76b8bb1fd900b136ac752a306e215650f5e240ca')

package() {
	cd "$srcdir"

	install -Dm755 "$srcdir/swayidle.sh" "$pkgdir/usr/lib/swayidle/swayidle-users"
	install -Dm644 "$srcdir/swayidle.service" "$pkgdir/usr/lib/systemd/user/swayidle.service"
}
# vim: set ts=4 sw=0 noexpandtab autoindent :
