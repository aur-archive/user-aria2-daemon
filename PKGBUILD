# Maintainer: Guten Ye

pkgname="user-aria2-daemon"
pkgver=0.1
pkgrel=6
pkgdesc="an aria2 user daemon. READ https://github.com/GutenYe/user-daemon-system FIRST"
arch=("i686" "x86_64")
url="http://aria2.sourceforge.net"
license=("MIT")
depends=("user-daemon-system-git" "aria2")
backup=("home/$USER/etc/conf.d/aria2")
source=("rc.aria2"
        "conf.aria2")

package() {
  cd "$srcdir"

  install -Dm755 rc.aria2 "$pkgdir/home/$USER/etc/rc.d/aria2"
  install -Dm644 conf.aria2 "$pkgdir/home/$USER/etc/conf.d/aria2"

  chown $USER:$USER -R "$pkgdir/home/$USER"
}

# vim:set ts=2 sw=2 et:
md5sums=('a4fa553a2b1ce86c4f3556e46a7e6e64'
         '25389fb9ba3a57078050475d7443c94b')
