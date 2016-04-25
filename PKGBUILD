pkgname=gitkraken
pkgver=1.1.0
pkgrel=2
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
sha256sums=('4d5205d64302e23d2d8f89cbd9ff40027d4c4a1e549f446b93d86aef667a89d6')
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
