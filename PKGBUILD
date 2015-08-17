# Contributor: John D Jones III <j[nospace]n[nospace]b[nospace]e[nospace]k[nospace]1972 -_AT_- the domain name google offers a mail service at ending in dot com>
# Generator  : CPANPLUS::Dist::Arch 1.25

pkgname='perl-net-smtp-tls-butmaintained'
pkgver='0.24'
pkgrel='1'
pkgdesc="An SMTP client supporting TLS and AUTH (DEPRECATED, use Net::SMTPS instead)"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-digest-hmac' 'perl-io-socket-ssl>=1.76' 'perl-net-ssleay')
makedepends=()
url='http://search.cpan.org/dist/Net-SMTP-TLS-ButMaintained'
source=('http://search.cpan.org/CPAN/authors/id/F/FA/FAYLAND/Net-SMTP-TLS-ButMaintained-0.24.tar.gz')
md5sums=('45cc8ac31dff1f06ff4bdcdf4d88afdb')
sha512sums=('28c5145ed5a3ce2beecbe95dde33c6892a4384102f0fe7c795bc92206e34257cae5c993e8c748b462c87a494eab399e45e56737bc3c424aa155613bbee2e4588')
_distdir="Net-SMTP-TLS-ButMaintained-0.24"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install

  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
