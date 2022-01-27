# Maintainer: 7thCore

pkgname=mcsrv-script
pkgver=1.2
pkgrel=6
pkgdesc='Minecraft server script for running the server on linux.'
arch=('x86_64')
license=('GPL3')
depends=('bash'
         'coreutils'
         'sudo'
         'grep'
         'sed'
         'awk'
         'curl'
         'rsync'
         'wget'
         'findutils'
         'tmux'
         'jq'
         'zip'
         'unzip'
         'p7zip'
         'postfix'
         'jre-openjdk-headless')
install=mcsrv-script.install
source=('bash_profile'
        'mcsrv-forge@.service'
        'mcsrv-mkdir-tmpfs@.service'
        'mcsrv-script.bash'
        'mcsrv-send-notification@.service'
        'mcsrv-serversync@.service'
        'mcsrv-spigot@.service'
        'mcsrv-timer-1.service'
        'mcsrv-timer-1.timer'
        'mcsrv-timer-2.service'
        'mcsrv-timer-2.timer'
        'mcsrv-tmpfs-forge@.service'
        'mcsrv-tmpfs-spigot@.service'
        'mcsrv-tmpfs-vanilla@.service'
        'mcsrv-vanilla@.service')
sha256sums=('f1e2f643b81b27d16fe79e0563e39c597ce42621ae7c2433fd5b70f1eeab5d63'
            '50c70f7cf8f487bee40628d8254f87c3c5957fd627cbbc3ad241538736348e84'
            '85792a07aa66663a8428006e454c7949c932a0f0796ccf60111c1a368a845fb8'
            '3fd3a6706dce097d3327151ea3991285b42f51320a84b9f73a36f1ab518de779'
            '0e533328a50d12981fc0624288234821175b5970363a6e2ba1de50bc0b2ccb8e'
            '5dc94b0c608f3662641e1cad2880dbbc0ec379ebe64ddd0b0bdd913053d79c19'
            '6c353644cd3ab56a258fa2cb490897c7338c8248347c54c41e09ffa7ca3dee5b'
            '21b627f1fb96a41bbd084bac92a99d0f94085a07d9acb8c01f15007535feef10'
            '5116c82874543bd11f4976495fb30075fd076115ad877fcecb8e1a6a97f5471e'
            'e96dd020900db19d3932d5f83a69cad0222ccfdc99f72e6be57ebfb32fbedf6f'
            '59bb73d65729d1b8919d3ed0b3cbc7603b42499a1cdd7aaa5ad9f96d733f531b'
            '149ba38e335c70e47a5a1f5c21e8be599b38c5211158a102f1a1578b004e44e8'
            '048d4dbbf2a211d51ebbdf37eb769ff6561f5875a506824236aa1f01a3397cf7'
            'c54cc4aeb7f23e8989940939922582644db5741be1ae5f417a40f3c0389818cd'
            '38a7e44678aebf74cb4a483c816b4ba663ee364b009fb0660cee8e488d7f6b1a')

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
