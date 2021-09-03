# Maintainer: Rafael <rafael@rebornos.org>

pkgname=cnchi-urlfix
_pkgname=extra.py
_pkgname2=arch-release
_pkgname3=101_gnome.gschema.override
pkgver=20210903
pkgrel=1
pkgdesc="RebornOS cnchi url check fix, and other fixes."
arch=('any')
url="https://gitlab.com/rebornos-team/installers/cnchi/code"
license=('GPL3')
backup=('usr/share/cnchi/src/misc/extra.py'
         'etc/arch-release')
source=("${_pkgname}"
        "${_pkgname2}"
        "${_pkgname3}")
sha256sums=('de02ab5dc41c52acbaa2391dce3d976fe5160a5b9d51a0f2cc9c5d7682e4bd7f'
            '1564a243cac7435420cbd1a5a1d40a00f6781637c29243f6328902370837ffe1'
            'c38a3ca307e70d8f868c6854783e690b7fc297379fe4dfad76b7c8fe75c2dfc0')
install=${pkgname}.install

pkgver() {
    date +%Y%m%d
}

package() {
    mkdir -p ${pkgdir}/usr/share/cnchi/src/misc/
    mkdir -p ${pkgdir}/etc
    install -Dm644 ${srcdir}/${_pkgname} ${pkgdir}/usr/share/cnchi/src/misc/${_pkgname}-newer
    install -Dm644 ${srcdir}/${_pkgname2} ${pkgdir}/etc/${_pkgname2}-newer
    install -Dm644 ${srcdir}/${_pkgname3} ${pkgdir}/usr/share/cnchi/${_pkgname3}-newer
}

