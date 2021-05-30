pkgname=(tweaks-phosh tweaks-plasma-mobile tweaks-lomiri tweaks-desktop-files)
pkgbase=tweaks
pkgver=0.4
pkgrel=2
arch=(any)
license=(Unlicense)
source=(desktop-files.sh
        osk-wayland
        avahi-discover.desktop
        bssh.desktop
        bvnc.desktop
        nm-connection-editor.desktop
        org.gnome.Extensions.desktop
        org.gnome.Shell.Extensions.desktop
        org.gnome.Terminal.desktop
        qv4l2.desktop
        qvidcap.desktop
        UserFeedbackConsole.desktop
        xgps.desktop
        xgpsspeed.desktop)
sha256sums=('ec179d4e0ab7cb473f95d77d553a00c8fa056bd80c3080eea1e044a5b1ae5287'
            '25ed5a35cd3faa2a3385266e937ad3a38ab1b549aebc386894ff91bf93c6b776'
            'ace41d2fc2969fdee0d6e820ff5ed863c5977aaa60c0eeb072ff46b5ea26a3ea'
            '959d5fc49c3b6d3b18dc87083f300d34824e027cb7b11cc63061b80088abfe04'
            'f8554e9c68338e94e15cee9de48b35281cb08be2ddf517548a65b485006af3cc'
            '978ec2134bf65d2a5d1075eea9bdf48de80661e69e9d60c52f4855f02a918970'
            '5282652abc7caa1abcd871b34ba407ab91982cd0326291c1b4019ed0db0cce07'
            'fcbbe40f99432d8e9873f10dc7b1143d51c78ae50d3c22c6f3357a454f3f84e5'
            'df9e4f88e5c5a3b1f451dc0dc11d74365d673b63ef370b802507924e8ae4661b'
            '69933cc943f0e5b257da0b62d4b2eb5116e0e210af4ac8d9dc0a246879c6206f'
            '91b584c062e11d44620803bd06ad67e5cf33b214f28a8998b6a51ab0e08cc0b6'
            'b06524a2507b5bec24c3b11fec422c2a844cbf872bbf942d3ce1c979f03ee6a7'
            '9562002bc4be3b92d5904533e92d420a4435e71c5bdb85a1edce666e0d566a22'
            '4dc0755b4125e2c7ac21da83ebc7a66affed99e7af044af0559b79c48bd33b6f'
)

package_tweaks-desktop-files() {
  install -Dm755 "$srcdir"/desktop-files.sh "$pkgdir"/etc/profile.d/desktop-files.sh
  mkdir -p "$pkgdir"/usr/share/tweaks-desktop-files/applications
	cp "$srcdir"/*.desktop "$pkgdir"/usr/share/tweaks-desktop-files/applications/
}

package_tweaks-phosh() {
  depends=(modemmanager phosh zswap-arm)
  install=phosh.install
  install -Dm755 "$srcdir"/osk-wayland "$pkgdir"/usr/bin/osk-wayland
}
package_tweaks-plasma-mobile() {
  depends=(sddm modemmanager tlp zswap-arm kscreen)
  install=plasma-mobile.install
}
package_tweaks-lomiri() {
  depends=(lightdm-lomiri deviceinfo modemmanager tlp zswap-arm repowerd hfd-service sensorfw-git)
  install=lomiri.install
}