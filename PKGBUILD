# Maintainer: Yaohan Chen <yaohan.chen@gmail.com>

pkgname=hib-dlagent-phantomjs-git
_appname=hib-dlagent
pkgver=0.6.9.gafc97d7
pkgrel=1
pkgdesc='Tool to download Humble Indie Bundle binaries by file name (uses PhantomJS to support new Humble Bundle site)'
arch=('any')
url='https://github.com/hagabaka/hib-dlagent'
license=('GPL2')
depends=('curl' 'phantomjs' 'imagemagick')
makedepends=('git')
provides=("$_appname")
conflicts=("$_appname")
backup=('etc/hib-dlagent/phantomjs-config.json')
optdepends=('gnome-keyring-query: encrypted account password support')
source=('git+https://github.com/hagabaka/hib-dlagent.git')
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/$_appname"
  git describe --tags | sed 's/^v//; s/-/./g'
}

package() {
  cd "$srcdir/$_appname"
  DEST="$pkgdir" ./install.sh
}
