# Maintainer: x1b6e6 <ftdabcde@gmail.com>

pkgname=swayidle-user
pkgver=1.0.1
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
)
sha1sums=('50531eb086689c27c974aef9776dc1811db30afb'
          '76b8bb1fd900b136ac752a306e215650f5e240ca')

package() {
	cd "$srcdir"

	install -Dm755 "$srcdir/swayidle.sh" "$pkgdir/usr/lib/swayidle/swayidle-users"
	install -Dm644 "$srcdir/swayidle.service" "$pkgdir/usr/lib/systemd/user/swayidle.service"
}
# vim: set ts=4 sw=0 noexpandtab autoindent :
