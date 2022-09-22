# Maintainer: Solomon Choina <shlomochoina@gmail.com>
# Maintainer: William Tumeo <github@tumeo.space>
pkgname=monodevelop-bin
_pkgver=7.8.4.1
pkgver=${_pkgver//[+-]/_}
pkgrel=4
pkgdesc="MonoDevelop is a GNOME IDE primarily designed for C# and other CLI (.NET) languages"
arch=('x86_64')
depends=('gtk-sharp-2' 'gtk-sharp-3' 'mono-msbuild')
optdepends=('fsharp: for building fsharp programs')
provides=('monodevelop')
conflicts=('monodevelop')
url="https://github.com/mono/monodevelop"
license=('MIT')
#source=("monodevelop-amd64-v${_pkgver}.deb::http://download.mono-project.com/repo/ubuntu/pool/main/m/monodevelop/monodevelop_7.8.4.1-0xamarin6+ubuntu1804b1_amd64.deb")
source=("monodevelop-amd64-v${_pkgver}.deb::https://github.com/williamd1k0/monodevelop/releases/download/monodevelop-${_pkgver}/monodevelop_${_pkgver}-0xamarin6+ubuntu1804b1_amd64.deb")
sha256sums=('e98cf23872aa0cb09fa000dd8f0ef9ad7f03a41a2d28ab1e2f215493bbd073bc')

package() {
    cd "${srcdir}"

    bsdtar xf data.tar.xz
    chmod -R g-w usr
    mv usr "${pkgdir}"
}
