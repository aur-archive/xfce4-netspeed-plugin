# Maintainer: kfgz <kfgz at interia dot pl>
# Maintainer: Vinycius Maia <suportevg at uol dot com dot br>

pkgname=xfce4-netspeed-plugin
pkgdesc="Netspeed plugin for xfce4 panel. Like gnome netspeed applet"
pkgver=0.3.1
pkgrel=1
arch=('i686' 'x86_64')
url="http://code.google.com/p/xfce4-netspeed-plugin/"
license=('GPL')
depends=('xfce4-panel' 'libxfcegui4' 'libgtop')
makedepends=('intltool')
install=xfce4-netspeed-plugin.install
source=(http://xfce4-netspeed-plugin.googlecode.com/files/${pkgname}-${pkgver}.tar.gz
        xfce4-netspeed-plugin.install)
md5sums=('b88cacc3ecd53798d76855e35a7a4d79'
         'b2ebab59089be208323356fef393640a')

build() {
  cd "${srcdir}"/${pkgname}
  ./configure --prefix=/usr
  make
}

package(){
  cd "${srcdir}"/${pkgname}
  make DESTDIR="${pkgdir}" install
}
