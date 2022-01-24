# Maintainer: 7thCore

pkgname=mcsrv-script
pkgver=1.0
pkgrel=1
pkgdesc='Minecraft server script for running the server on linux.'
arch=('x86_64')
depends=('bash'
         'coreutils'
         'sudo'
         'grep'
         'sed'
         'awk'
         'curl'
         'rsync'
         'findutils'
         'unzip'
         'p7zip'
         'wget'
         'tmux'
         'postfix'
         'zip'
         'jq'
         'samba'
         'jre-openjdk-headless')
backup=('')
install=mcsrv-script.install
source=('mcsrv-script.bash'
        'mcsrv-timer-1.timer'
        'mcsrv-timer-1.service'
        'mcsrv-timer-2.timer'
        'mcsrv-timer-2.service'
        'mcsrv-send-notification@.service'
        'mcsrv-vanilla@.service'
        'mcsrv-forge@.service'
        'mcsrv-spigot@.service'
        'mcsrv-mkdir-tmpfs@.service'
        'mcsrv-tmpfs-vanilla@.service'
        'mcsrv-tmpfs-forge@.service'
        'mcsrv-tmpfs-spigot@.service'
        'mcsrv-serversync@.service'
        'bash_profile')
noextract=('')
sha256sums=('9a51538ca53b0d5f75b3245c2e18277737000f4c1fe298c0bee9489aa44e3a13'
            '4bf64f7a529c426d54e5cdd1cb97491d9187d0526fb78611f15d324c55a203bd'
            '9d846d83d7a6070f326761e9252a8cd0e1130d4e5983b8fccf4dd5bde5211d49'
            '7eefa11eb40c25bd18c6b4fb85abe2e887090a290c948980006d4ad9f25f2ddb'
            '2f21db90cbe469ce52466dbe85f67df21f1c899d456a902a1fafefd48826e99f'
            'dd10a8657ad0287cb8af5fe0bc76609a8844340aeb86035a252a5bbf47acdde7'
            '96b8c6498c1406284df0c648a76f0350449f5beee71523f9434bf30e62da2abe'
            '177bae6c347302067eddd52d2c32e819d152e443b3dc4fc70ed35945026d24b8'
            '2b6fa6b9fa173c3c2f91f818e3d139513078ce8f9a181e1d02a92ffe48b87d47'
            '80d949814a2a6b3cc86d4457b0060570e12bbd523aaf34dc60191e361f51a3c6'
            '7cfa80adffa9326e60c6ca3849747ae2b79e9dfd4b7645229378429e41d00bb7'
            'f1f346de0484938911688f50cc515551e1707a3e2d5c5a4917a563cdfc9a3e52'
            '97f5c7762c0c27993d439191f23b1365734bce276a60eb6c176cc1e0fde1003f'
            '774a77411c6f4fde56610cb3cbd2e09acd615467a9aa02974ac11dea35593b0d'
            'f1e2f643b81b27d16fe79e0563e39c597ce42621ae7c2433fd5b70f1eeab5d63')

package() {
  install -d -m0755 "${pkgdir}/usr/bin"
  install -d -m0755 "${pkgdir}/srv/mcsrv"
  install -d -m0755 "${pkgdir}/srv/mcsrv/config"
  install -d -m0755 "${pkgdir}/srv/mcsrv/updates"
  install -d -m0755 "${pkgdir}/srv/mcsrv/backups"
  install -d -m0755 "${pkgdir}/srv/mcsrv/logs"
  install -d -m0755 "${pkgdir}/srv/mcsrv/tmpfs"
  install -d -m0755 "${pkgdir}/srv/mcsrv/.config"
  install -d -m0755 "${pkgdir}/srv/mcsrv/.config/systemd"
  install -d -m0755 "${pkgdir}/srv/mcsrv/.config/systemd/user"
  install -D -Dm755 "${srcdir}/mcsrv-script.bash" "${pkgdir}/usr/bin/mcsrv-script"
  install -D -Dm755 "${srcdir}/mcsrv-timer-1.timer" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-timer-1.timer"
  install -D -Dm755 "${srcdir}/mcsrv-timer-1.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-timer-1.service"
  install -D -Dm755 "${srcdir}/mcsrv-timer-2.timer" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-timer-2.timer"
  install -D -Dm755 "${srcdir}/mcsrv-timer-2.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-timer-2.service"
  install -D -Dm755 "${srcdir}/mcsrv-send-notification@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-send-notification@.service"
  install -D -Dm755 "${srcdir}/mcsrv-vanilla@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-vanilla@.service"
  install -D -Dm755 "${srcdir}/mcsrv-forge@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-forge@.service"
  install -D -Dm755 "${srcdir}/mcsrv-spigot@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-spigot@.service"
  install -D -Dm755 "${srcdir}/mcsrv-mkdir-tmpfs@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-mkdir-tmpfs@.service"
  install -D -Dm755 "${srcdir}/mcsrv-tmpfs-vanilla@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-tmpfs-vanilla@.service"
  install -D -Dm755 "${srcdir}/mcsrv-tmpfs-forge@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-tmpfs-forge@.service"
  install -D -Dm755 "${srcdir}/mcsrv-tmpfs-spigot@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-tmpfs-spigot@.service"
  install -D -Dm755 "${srcdir}/mcsrv-serversync@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-serversync@.service"
  install -D -Dm755 "${srcdir}/bash_profile" "${pkgdir}/srv/mcsrv/.bash_profile"
}
