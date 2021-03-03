pkgname=(tweaks-phosh tweaks-plasma-mobile tweaks-lomiri)
pkgver=0.1
pkgrel=1
arch=(any)
license=(Unlicense)

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