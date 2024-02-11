arch=('any')
url='https://github.com/baldulin/dateclass'
license=('MIT')
pkgver=0.0.4
pkgrel=1
pkgname='python-dateclass'
_name=dateclass
makedepends=(python-build python-installer python-wheel)
source=("https://github.com/baldulin/dateclass/archive/refs/tags/$pkgver.tar.gz")
sha512sums=(8e021a540ae616d7e7a3ec51c588a85a9a155b4263976b6da7c90d59e72523e9ad2f43b09cbcd0ba071cdeca2e174f87c8011e75f9d45f9699119a6f8d990c4e)

build() {
    cd "$_name-$pkgver/"
    python -m build --wheel --no-isolation
}

package() {
    cd "$_name-$pkgver"
    python -m installer --destdir="$pkgdir" dist/dateclass-$pkgver-*.whl
}
