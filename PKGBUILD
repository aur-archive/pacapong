# Maintainer: Jozef Riha <jose1711 at gmail dot com>

pkgname=pacapong
pkgver=1.3
pkgrel=3
pkgdesc="game combining pong, pacman and space invaders"
arch=('i686' 'x86_64')
license=('unknown')
url="http://kingpenguin.itch.io/pacapong"
source=("pacapong_linux.zip::pacapong_linux.zip" "${pkgname}.sh" "${pkgname}.desktop")
nosource=(1)
md5sums=('658c091abea7305cd0a33d367c251cc3'
         '780236c531d6a9cdfa8bec22c2f9757b'
         'e2d8d6e33b04abf3161710df22d1098f')
depends_i686=(openal libxxf86vm glu libxrandr)
depends_x86_64=(lib32-openal lib32-glu)

package() {
    mkdir -p ${pkgdir}/usr/share/${pkgname}/assets
    install -Dm644 ${srcdir}/${pkgname}/assets/* ${pkgdir}/usr/share/${pkgname}/assets
    install -Dm755 ${srcdir}/${pkgname}/runner ${pkgdir}/usr/share/${pkgname}/runner
    install -Dm755 ${srcdir}/${pkgname}.sh ${pkgdir}/usr/bin/${pkgname}
    install -Dm644 $srcdir/${pkgname}/assets/icon.png $pkgdir/usr/share/pixmaps/${pkgname}.png
    install -Dm644 $srcdir/${pkgname}.desktop $pkgdir/usr/share/applications/${pkgname}.desktop

}
