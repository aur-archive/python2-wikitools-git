# Contributor: Rémi Audebert <quaero.galileo@gmail.com>
# Contributor: Semyon Maryasin <symeon@maryasin.name>

pkgname=python2-wikitools-git
_pkgname=wikitools
pkgver=0.r366.8f7b6a8
pkgrel=1
pkgdesc="Python scripts and modules to interact with the MediaWiki API"
arch=('any')
url="https://github.com/alexz-enwp/wikitools"
license=('cc-by-sa-3.0' 'GPL3')
depends=('python2>=2.6')
optdepends=('python-poster: file upload support')
makedepends=('git')
source=('git://github.com/alexz-enwp/wikitools.git')
md5sums=('SKIP')
provides=('python2-wikitools')
conflicts=('python2-wikitools' 'python2-wikitools-svn')

pkgver() {
	cd "$srcdir/$_pkgname"
	printf "0.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
    cd "$srcdir/$_pkgname"

    msg "Starting setup.py..."
    python2 setup.py install --root=$pkgdir/ --optimize=1
}
