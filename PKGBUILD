# Maintainer: Marc Straube <m.straube@skunk-coding.de>

pkgname=policyd-weight
pkgdesk="Policy server for postfix"
pkgver=0.1.15_beta_2
pkgrel=1
arch=('i686' 'x86_64')
url="http://policyd-weight.org"
license=('GPL')
depends=('perl' 'perl-net-dns')
install='policyd-weight.install'
source=('http://policyd-weight.org/policyd-weight'
  'fix-dn_expand.patch')
sha256sums=('ef15bc87a84e8bfb9adf18ffc8fa02449600725aec6bd2d2e5bf1c153d24820b'
  'cdf2112114b03ee1a3a39dd3795ea880ccda2ca94a1e97d66663eee16a64161c')

prepare() {
  cd "${srcdir}/"
  patch -Np1 -i ${pkgname}.patch ${pkgname}
}

package() {
  cd "$srcdir/"
  install -D -m550 ${pkgname} "${pkgdir}/usr/bin/${pkgname}"
}
