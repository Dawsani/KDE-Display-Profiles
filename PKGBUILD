pkgname=kde-display-profiles
pkgver=1.0.0
pkgrel=1
pkgdesc="Display profile manager that uses kscreen-doctor to save and load display profiles on KDE Plasma."
arch=('any')
url="https://github.com/Dawsani/KDE-Display-Profiles"
license=('MIT')
depends=('python' 'python-pyqt6')
source=("$pkgname-$pkgver.tar.gz::https://github.com/username/myapp/archive/v$pkgver.tar.gz")
sha256sums=('SKIP')

package() {
    cd "$srcdir/myapp-$pkgver"

    install -Dm755 main.py "$pkgdir/usr/bin/myapp"

    install -Dm644 icon.png \
      "$pkgdir/usr/share/icons/hicolor/128x128/apps/myapp.png"

    install -Dm644 README.md \
      "$pkgdir/usr/share/doc/myapp/README.md"
}