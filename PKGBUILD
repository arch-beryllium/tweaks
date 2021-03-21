pkgname=(tweaks-phosh tweaks-plasma-mobile tweaks-lomiri tweaks-desktop-files)
pkgbase=tweaks
pkgver=0.1
pkgrel=1
arch=(any)
license=(Unlicense)
source=(desktop-files.sh)
sha256sums=('ec179d4e0ab7cb473f95d77d553a00c8fa056bd80c3080eea1e044a5b1ae5287')
makedepends=(kuserfeedback gnome-shell avahi gpsd v4l-utils nm-connection-editor gnome-terminal)

package_tweaks-desktop-files() {
  install -Dm755 "$srcdir"/desktop-files.sh "$pkgdir"/etc/profile.d/desktop-files.sh
  mkdir -p "$pkgdir"/usr/share/tweaks-desktop-files/applications
  cp /usr/share/applications/UserFeedbackConsole.desktop "$srcdir"
  cp /usr/share/applications/avahi-discover.desktop "$srcdir"
  cp /usr/share/applications/bssh.desktop "$srcdir"
  cp /usr/share/applications/bvnc.desktop "$srcdir"
  cp /usr/share/applications/nm-connection-editor.desktop "$srcdir"
  cp /usr/share/applications/org.gnome.Extensions.desktop "$srcdir"
  cp /usr/share/applications/org.gnome.Terminal.desktop "$srcdir"
  cp /usr/share/applications/qv4l2.desktop "$srcdir"
  cp /usr/share/applications/qvidcap.desktop "$srcdir"
  cp /usr/share/applications/xgps.desktop "$srcdir"
  cp /usr/share/applications/xgpsspeed.desktop "$srcdir"
  for file in "$srcdir"/*.desktop; do
    echo "NoDisplay=true" >> $file
  done
	cp "$srcdir"/*.desktop "$pkgdir"/usr/share/tweaks-desktop-files/applications/
}

package_tweaks-phosh() {
  depends=(lightdm modemmanager phosh zswap-arm)
  install=phosh.install
}
package_tweaks-plasma-mobile() {
  depends=(sddm modemmanager tlp zswap-arm kscreen)
  install=plasma-mobile.install
}
package_tweaks-lomiri() {
  depends=(lightdm-lomiri deviceinfo modemmanager tlp zswap-arm repowerd hfd-service sensorfw-git)
  install=lomiri.install
}