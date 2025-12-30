# Maintainer: mirsella <mirsella@protonmail.com>
pkgname=wtp-bin
pkgver=2.5.1
pkgrel=1
pkgdesc="A powerful Git worktree CLI tool with automated setup, branch tracking, and smart navigation "
arch=('x86_64')
url="https://github.com/satococoa/wtp"
license=('MIT')
depends=('tar')
source=("https://github.com/satococoa/wtp/releases/download/v${pkgver}/wtp_${pkgver}_Linux_${arch}.tar.gz")
sha256sums=('d1c21affb79da42c97d8bc796a89bd67328e722d891c272e4ea6b8758b1f75ac')

package() {
	cd "${srcdir}"

	path="wtp_${pkgver}_Linux_${arch}"
	mkdir "$path"
	tar -xzf "$path.tar.gz" -C "$path"

	install -Dm755 "$path/wtp" "${pkgdir}/usr/bin/wtp"

	if [[ -f "$path/LICENSE" ]]; then
		install -Dm644 "$path/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
	fi
}
