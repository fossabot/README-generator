# Maintainer: Tom Meyers tom@pbfp.team
pkgname=readme-generator-git
pkgver=r18.0ccf95b
pkgrel=1
pkgdesc="A basic tool to generate modern readme's"
arch=(any)
url="https://github.com/F0xedb/README-generator"
_reponame="README-generator"
license=('GPL')

source=(
"git+https://github.com/F0xedb/README-generator.git")
md5sums=('SKIP')
makedepends=('git')

pkgver() {
  cd "$srcdir/$_reponame"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}


build() {
    return 0;
}

package() {
        cd "$srcdir/$_reponame"
        install -Dm755 readme-gen "$pkgdir"/usr/bin/readme-gen
        install -Dm644 demo "$pkgdir"/var/cache/readme/demo
}
