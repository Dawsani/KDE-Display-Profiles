# Maintainer: Dawson Matthews <dawsonwmatthews@proton.me>

pkgname=kde-display-profiles
pkgver=1.0.0
pkgrel=1
pkgdesc="Display profile manager that uses kscreen-doctor to save and load display profiles on KDE Plasma"
arch=('any')
url="https://github.com/Dawsani/KDE-Display-Profiles"
license=('MIT')
depends=('python' 'pyside6' 'libkscreen')
makedepends=('python-build' 'python-installer' 'python-setuptools' 'python-wheel')
source=("$pkgname-$pkgver.tar.gz::$url/archive/v$pkgver.tar.gz")
sha256sums=('SKIP')

build() {
  # We are already in $srcdir, no need to cd
  python -m build --wheel --no-isolation
}

package() {
  python -m installer --destdir="$pkgdir" dist/*.whl

  # Install desktop file
  install -Dm644 "$pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop"

  # Install license
  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
