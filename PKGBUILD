# Maintainer: mirsella <mirsella@protonmail.com>
pkgname=wtp-bin
pkgver=2.9.0
pkgrel=1
pkgdesc="A powerful Git worktree CLI tool with automated setup, branch tracking, and smart navigation "
arch=('x86_64')
url="https://github.com/satococoa/wtp"
license=('MIT')
depends=('tar')
source=("https://github.com/satococoa/wtp/releases/download/v${pkgver}/wtp_${pkgver}_Linux_${arch}.tar.gz")
sha256sums=('52ae2d28a5dded6075ab834ecee7f897dfdf8019668c0899c16bad406796ede1')

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
