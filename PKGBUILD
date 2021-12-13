pkgname=gitkraken
pkgver=8.2.0
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom: https://www.gitkraken.com/eula')
depends=('curl' 'gtk3' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libsecret')
optdepends=('openssh' 'gnupg')
source=("https://release.gitkraken.com/linux/GitKraken-v$pkgver.tar.gz"
        "${pkgname}.desktop"
        "${pkgname}.svg"
        "${pkgname}.sh")
md5sums=('2288e5cce376d675f2205e31adb5f998'
         'e70ed2fa89e0929c02262f9300f0f1b2'
         '952efc24804093bec7a95efe02d18c48'
         '2988e132d79a4f2dbe6205d538c513d6')

package() {
    install -dm755 ${pkgdir}/opt/${pkgname} \
            ${pkgdir}/usr/share/{applications,icons/hicolor/scalable/apps} \
            ${pkgdir}/usr/bin
    cp -R ${srcdir}/${pkgname}/* ${pkgdir}/opt/${pkgname}
    chmod 4755 ${pkgdir}/opt/${pkgname}/chrome-sandbox
    install -Dm755 ${srcdir}/${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 ${srcdir}/${pkgname}.desktop \
            ${pkgdir}/usr/share/applications/${pkgname}.desktop
    install -Dm644 ${srcdir}/${pkgname}.svg \
            ${pkgdir}/usr/share/icons/hicolor/scalable/apps/${pkgname}.svg
}
