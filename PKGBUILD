# Maintainer: Your Name <your.email@example.com>
pkgname=ueransim
pkgver=3.2.6
pkgrel=1
pkgdesc="Open source 5G UE and RAN (gNodeB) simulator"
arch=('amd64')
url="https://github.com/aligungr/UERANSIM"
license=('GPL3')
depends=('libsctp1' 'lksctp-tools' 'iproute2')
makedepends=('gcc' 'g++' 'make' 'cmake' 'git')
source=("${pkgname}-${pkgver}::git+https://github.com/aligungr/UERANSIM.git#tag=v${pkgver}")
sha256sums=('SKIP')

prepare() {
    cd "${pkgname}-${pkgver}"
    # No preparation needed
}

build() {
    cd "${pkgname}-${pkgver}"
    make
}

package() {
    cd "${pkgname}-${pkgver}"
    
    # Install binaries
    install -Dm755 build/nr-gnb "${pkgdir}/usr/bin/nr-gnb"
    install -Dm755 build/nr-ue "${pkgdir}/usr/bin/nr-ue"
    install -Dm755 build/nr-cli "${pkgdir}/usr/bin/nr-cli"
    install -Dm755 build/nr-binder "${pkgdir}/usr/bin/nr-binder"
    
    # Install library
    install -Dm755 build/libdevbnd.so "${pkgdir}/usr/lib/libdevbnd.so"
    
    # Install configuration examples
    install -dm755 "${pkgdir}/usr/share/ueransim/config"
    cp -r config/* "${pkgdir}/usr/share/ueransim/config/"
    
    # Install documentation
    install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README.md"
    install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}

# vim: ts=4 sw=4 et:
