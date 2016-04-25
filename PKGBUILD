pkgname=gitkraken
pkgver=1.2.0
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
sha256sums=('701166483d36996c29891f752d6c1093e51a9010567339d1a36c8ad9dae41f3b')
source=("https://release.gitkraken.com/linux/gitkraken-amd64.deb")
install=gitkraken.install
package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/app/gitkraken/' "$pkgdir/usr/share/applications/$pkgname.desktop"
  rm -r $pkgdir/usr/share/{lintian,doc}
  cd $pkgdir/usr/share/pixmaps
  mv app.png  gitkraken.png
}
