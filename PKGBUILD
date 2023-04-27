# Maintainer: Narazaka <info@narazaka.net>

pkgname=mediamtx
_pkgver=0.22.2
pkgver="${_pkgver}"
pkgrel=1
pkgdesc="ready-to-use RTSP / RTMP / LL-HLS / WebRTC server and proxy that allows to read, publish and proxy video and audio streams."
arch=('x86_64')
url="https://github.com/aler9/mediamtx"
license=('MIT')
depends=()
conflicts=()
backup=('etc/conf.d/mediamtx.yml')

source=("https://github.com/aler9/mediamtx/releases/download/v${_pkgver}/mediamtx_v${_pkgver}_linux_amd64.tar.gz"
	"mediamtx.service"
	"mediamtx.sysusers")

package() {
	install -Dm644 mediamtx.yml              "${pkgdir}/etc/conf.d/${pkgname}.yml"
	install -Dm755 mediamtx                  "${pkgdir}/usr/bin/${pkgname}"
	install -Dm644 mediamtx.service          "${pkgdir}/usr/lib/systemd/system/${pkgname}.service"
	install -Dm644 mediamtx.sysusers         "${pkgdir}/usr/lib/sysusers.d/${pkgname}.conf"
	install -D LICENSE                       "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

sha256sums=('02d97574ad79afac44a97e564f18eea6dd58e832d4b66be804a2b8831cd5dc0f'
            '5ea0d8d1e868e3a25e826bf42b53debf4cc967863313209cc6d0181837378deb'
            '3460301de60880b4c8f8079b825d6c7a03ed3f152e0649106d1e810f1f5e93d7')
