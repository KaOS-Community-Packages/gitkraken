pkgname=gitkraken
pkgver=1.9.0
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
source=("https://release.gitkraken.com/linux/gitkraken-amd64.deb")
md5sums=('b3dc5ff7dd02877fef4561ffe931dec4')
package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/app/gitkraken/' "$pkgdir/usr/share/applications/$pkgname.desktop"
  rm -r $pkgdir/usr/share/{lintian,doc}
  cd $pkgdir/usr/share/pixmaps
  mv app.png  gitkraken.png
}
