# Maintainer: mirsella <mirsella@protonmail.com>
pkgname=wtp-bin
pkgver=2.8.0
pkgrel=1
pkgdesc="A powerful Git worktree CLI tool with automated setup, branch tracking, and smart navigation "
arch=('x86_64')
url="https://github.com/satococoa/wtp"
license=('MIT')
depends=('tar')
source=("https://github.com/satococoa/wtp/releases/download/v${pkgver}/wtp_${pkgver}_Linux_${arch}.tar.gz")
sha256sums=('4e4c7033f8de54565edb6f3803d3bffabd0226f57b22a387068cb70bedc195a4')

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
