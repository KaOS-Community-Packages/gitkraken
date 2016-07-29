pkgname=gitkraken
pkgver=1.5.1
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('custom')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib' 'libgnome-keyring')
md5sums=('a213b897a99685a6a809d4467b184079')
source=("https://release.gitkraken.com/linux/gitkraken-amd64.deb")
package() {
  tar -xzf ${srcdir}/data.tar.gz -C "${pkgdir}"
  chmod -R 755 "$pkgdir/usr"
  sed -i  's/app/gitkraken/' "$pkgdir/usr/share/applications/$pkgname.desktop"
  rm -r $pkgdir/usr/share/{lintian,doc}
  cd $pkgdir/usr/share/pixmaps
  mv app.png  gitkraken.png
}
