# Maintainer: 7thCore

pkgname=mcsrv-script
pkgver=1.3
pkgrel=5
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
        'mcsrv-mkdir-tmpfs@.service'
        'mcsrv-script.bash'
        'mcsrv-send-notification@.service'
        'mcsrv-serversync@.service'
        'mcsrv@.service'
        'mcsrv-timer-1.service'
        'mcsrv-timer-1.timer'
        'mcsrv-timer-2.service'
        'mcsrv-timer-2.timer'
        'mcsrv-tmpfs@.service')
sha256sums=('f1e2f643b81b27d16fe79e0563e39c597ce42621ae7c2433fd5b70f1eeab5d63'
            '85792a07aa66663a8428006e454c7949c932a0f0796ccf60111c1a368a845fb8'
            '2599450eaf211417299d103c7803511352ef0356bc70b442311e23c2d599e4df'
            '0e533328a50d12981fc0624288234821175b5970363a6e2ba1de50bc0b2ccb8e'
            '5dc94b0c608f3662641e1cad2880dbbc0ec379ebe64ddd0b0bdd913053d79c19'
            '257952bb07922e11fc215f61ec9d9173ef2d571cd5b835653c7fc2ad8e954c1c'
            '21b627f1fb96a41bbd084bac92a99d0f94085a07d9acb8c01f15007535feef10'
            '5116c82874543bd11f4976495fb30075fd076115ad877fcecb8e1a6a97f5471e'
            'e96dd020900db19d3932d5f83a69cad0222ccfdc99f72e6be57ebfb32fbedf6f'
            '59bb73d65729d1b8919d3ed0b3cbc7603b42499a1cdd7aaa5ad9f96d733f531b'
            '066ae9068d9cc745ade3427263c77ada2323de5a0daf3d41e5bc8fefcaeeb460')

package() {
  install -d -m0755 "${pkgdir}/usr/bin"
  install -d -m0755 "${pkgdir}/srv/mcsrv"
  install -d -m0755 "${pkgdir}/srv/mcsrv/server"
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
  install -D -Dm755 "${srcdir}/mcsrv@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv@.service"
  install -D -Dm755 "${srcdir}/mcsrv-mkdir-tmpfs@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-mkdir-tmpfs@.service"
  install -D -Dm755 "${srcdir}/mcsrv-tmpfs@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-tmpfs@.service"
  install -D -Dm755 "${srcdir}/mcsrv-serversync@.service" "${pkgdir}/srv/mcsrv/.config/systemd/user/mcsrv-serversync@.service"
  install -D -Dm755 "${srcdir}/bash_profile" "${pkgdir}/srv/mcsrv/.bash_profile"
}
