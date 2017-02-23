pkgname=gitkraken
pkgver=2.1.0
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom')
depends=('gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
source=("https://release.gitkraken.com/linux/v${pkgver}.tar.gz"
        "${pkgname}.desktop"
        "${pkgname}.svg")
md5sums=('075de0a5610f6dc488563fe769d731c6'
         'e70ed2fa89e0929c02262f9300f0f1b2'
         '952efc24804093bec7a95efe02d18c48')

package() {
    install -dm755 ${pkgdir}/opt/${pkgname} \
            ${pkgdir}/usr/share/{applications,icons/hicolor/scalable/apps} \
            ${pkgdir}/usr/bin
    cp -R ${srcdir}/${pkgname}/* ${pkgdir}/opt/${pkgname}
    ln -s /opt/${pkgname}/${pkgname} ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${srcdir}/${pkgname}.desktop \
            ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 ${srcdir}/${pkgname}.svg \
            ${pkgdir}/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg
}
