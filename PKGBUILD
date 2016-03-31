pkgname=gitkraken
pkgver=1.0.0
pkgrel=1
pkgdesc="Git client with efficiency, elegance and reliability at the core"
arch=('x86_64')
url="https://www.gitkraken.com/"
license=('GitHub')
depends=('systemd' 'gconf' 'gtk2' 'nss' 'libxtst' 'libnotify' 'alsa-lib')
sha256sums=('6926c3b6a7963c38b93c9c9f16ca741c8b843f9a93c6e2323413a2c217088ef3')
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
