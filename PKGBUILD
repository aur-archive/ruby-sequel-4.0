# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Thomas Gubler <thomasgubler@gmail.com>

_gemname=sequel
pkgname=ruby-$_gemname-4.0
pkgver=4.0.0
pkgrel=1
pkgdesc='The Database Toolkit for Ruby'
arch=(any)
url='http://sequel.rubyforge.org'
license=()
depends=(ruby)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('c24ecbfb477590828276672e1c0e2d43a90cd9bc')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
  # non-HEAD version should not install any files in /usr/bin
  rm -r "$pkgdir/usr/bin/"
}
