# Contributor: Francisco Josué Morazán Arriola, https://github.com/fjmorazan
# Contributor: Widi Rajaka Untung, https://github.com/wrajaka
# Contributor: Colin Duquesnoy, https://github.com/ColinDuquesnoy
# Contributor: DemianRV, https://github.com/DemianRV
# Contributor: forostm, https://github.com/forostm
# Contributor: dagodax, https://github.com/dagodax
# Contributor: Mermouy, https://github.com/Mermouy
# Contributor: Gunther Strube, https://github.com/bits4fun

pkgname=gitkraken
pkgver=4.0.5
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom: https://www.gitkraken.com/eula')
depends=('curl-kcp' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
source=("https://release.axocdn.com/linux/gitkraken-amd64.tar.gz"
        "${pkgname}.desktop"
        "${pkgname}.svg"
        "${pkgname}.sh")
md5sums=('d23a48ba5c6a25887156c81fca34b1dd'
         'e70ed2fa89e0929c02262f9300f0f1b2'
         '952efc24804093bec7a95efe02d18c48'
         '10af5f5f6e5253f3b742982ebde6c1ae')

package() {
    install -dm755 ${pkgdir}/opt/${pkgname} \
            ${pkgdir}/usr/share/{applications,icons/hicolor/scalable/apps} \
            ${pkgdir}/usr/bin
    cp -R ${srcdir}/${pkgname}/* ${pkgdir}/opt/${pkgname}
    install -Dm755 ${srcdir}/${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${srcdir}/${pkgname}.desktop \
            ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 ${srcdir}/${pkgname}.svg \
            ${pkgdir}/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg
}
