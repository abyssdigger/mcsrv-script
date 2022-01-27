# Maintainer: 7thCore

pkgname=mcsrv-script
pkgver=1.2
pkgrel=3
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
            'b3f4ba2d85adc3f77e85ed704f78ba3fcf603485b42bd24fdfe0eb7cf4c7233f'
            '85792a07aa66663a8428006e454c7949c932a0f0796ccf60111c1a368a845fb8'
            'c5f7eaac20a050fbb62ba13fb4957da4d2e6255f25cd0f5fd3b04e30ccf77ed6'
            '0e533328a50d12981fc0624288234821175b5970363a6e2ba1de50bc0b2ccb8e'
            '0053895ef4c8d43715a3f8641b2381dca36717fa2f30f0db0f0606616088c460'
            'b9ea717b05244d78c136e05c7d340903fa81986a96dd47d8ce2294a0670e63e2'
            '21b627f1fb96a41bbd084bac92a99d0f94085a07d9acb8c01f15007535feef10'
            '5116c82874543bd11f4976495fb30075fd076115ad877fcecb8e1a6a97f5471e'
            'e96dd020900db19d3932d5f83a69cad0222ccfdc99f72e6be57ebfb32fbedf6f'
            '59bb73d65729d1b8919d3ed0b3cbc7603b42499a1cdd7aaa5ad9f96d733f531b'
            'ce00da21a2f9dba358a3bdce27066b9c8f42186cd2eb1e8817ac6060f4597c0f'
            '27748d2a37d53b59e8cd4cc458c73dc4d9a6ea6610a8479fd8bae5b782fbf3a9'
            '62c90d01871e46f4d17ef68dcd7c8ee48975cd78dfdcee43778418ff576782f5'
            'b56230e261d1123db9bd0fcad04c81456691bdda9904021892d1d42b9d6f3212')

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
