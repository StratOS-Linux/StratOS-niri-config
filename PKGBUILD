# Maintainer: @magitian <magitian@duck.com>
pkgname=stratos-niri-config
pkgver=1.0
pkgrel=3
pkgdesc="Niri configuration for StratOS"
arch=('any')
license=('GPL3')
conflicts=('stratos-hyprland-config')
depends=(
    'bluez-utils'
    'niri'
    'libpulse'
    'xdg-desktop-portal-gnome'
    'ttf-jetbrains-mono'
    'ttf-jetbrains-mono-nerd'
    'swaync'
    'hyprpaper'
    'hypridle'
    'brightnessctl'
    'rofi'
    'grim'
    'slurp'
    'stratos-wallpapers'
    'stratos-waybar-niri-config'
    'swappy'
    'wl-clipboard'
    'xwayland-satellite'
)

optdepends=(
    'ghostty: alternative terminal emulator to Kitty'
    'alacritty: blazingly fast terminal emulator written in Rust'
    "nautilus: GNOME's file manager"
    'swaybg: alternative wallpaper utility'
    'libqalculate: command-line scientific calculator, needed for calc script'
    'stratos-kitty-config: kitty config'
    'stratos-eww-config: eww config'
)

source=()
install=stratos-niri-config.install

prepare() {
    cp -r "$startdir/.config/" "$srcdir/"
}

package() {
    install -d "$pkgdir/etc/skel/.config"
    cp -r "$srcdir/.config/niri/" "$pkgdir/etc/skel/.config/"
    cp -r "$srcdir/.config/hypr/" "$pkgdir/etc/skel/.config/"
}
