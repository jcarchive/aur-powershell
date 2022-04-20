# Maintainer: Jose C.

pkgname=powershell
pkgver='v7.2.2'
pkgrel=1
#pkgdesc='powershell is a multiplatform shell'
arch=('x86_64')
options=('!strip' 'staticlibs')
url='https://github.com/PowerShell'
license=('Commercial')
optdepends=('mono: Free implementation of the .NET platform including runtime and compiler', 'dotnet-sdk: The .NET Core SDK')
provides=('pwsh')
conflicts=('pwsh')

_filename="powershell-7.2.2-linux-x64.tar.gz"
_filextract="$pkgname-$pkgver"

source=("https://github.com/PowerShell/PowerShell/releases/download/v7.2.2/powershell-7.2.2-linux-x64.tar.gz"
)

sha256sums=( '3f6b3c1a9391e0c23e06e534da321e12ae883a64d99cb1dd738b274d97075891')

prepare() {
  files=$(tar -tf $_filename | cut -d/ -f2 | uniq)
  mkdir $_filextract
  mv  $files $srcdir/$_filextract/
}

package() {
	#Create directories with permission rwxr-xr-x
	install -m755 -d "${pkgdir}/usr/share" "${pkgdir}/usr/bin"

	#Copy files to pkg destination
	cp -r "${srcdir}/${_filextract}" "${pkgdir}/usr/share/${pkgname}"
  chown -R root:root "${pkgdir}/usr/share/${pkgname}"

	ln -s "/usr/share/${pkgname}/pwsh" "${pkgdir}/usr/bin/pwsh"
}
