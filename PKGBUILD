# Contributor: Médéric Boquien <mboquien@free.fr>

pkgname=python-pywcs
pkgver=1.11
pkgrel=2
pkgdesc="A python language interface to handle FITS WCS"
arch=('i686' 'x86_64')
url="http://stsdas.stsci.edu/astrolib/pywcs/"
license=("custom")
depends=('python2' 'python2-pyfits>=1.4' 'python2-numpy>=1.3')
source=("http://stsdas.stsci.edu/astrolib/pywcs-$pkgver-4.8.2.tar.gz")
md5sums=('0721ceb7d8270868dd5d688ba60e4089')

build() {
  cd $srcdir/pywcs-$pkgver-4.8.2
  python2 setup.py install --root=$pkgdir/ --optimize=1 || return 1

  # Remember to install licenses if the license is not a common license!
  install -D -m644 $srcdir/pywcs-$pkgver-4.8.2/LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
}
