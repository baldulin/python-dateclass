arch=('any')
url='https://github.com/baldulin/dateclass'
license=('MIT')
pkgver=0.0.2
pkgrel=1
pkgname='python-dateclass'
_name=dateclass
makedepends=(python-build python-pip)
source=("https://github.com/baldulin/dateclass/archive/refs/tags/$pkgver.tar.gz")
sha512sums=(1f0660bf17323c1a79ca40bfcc4b47d584b734c1b404865c874bc3ec4baa9ca8578eec88bb1ffd8c102d8f1e38b48cb08965ccbed1feddbc0c8c390743e98e80)

build() {
    cd "$_name-$pkgver/"
    python -m build
}

package() {
    cd "$_name-$pkgver"
    pip install "dist/dateclass-$pkgver.tar.gz" --break-system-packages
}
