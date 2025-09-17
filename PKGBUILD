# Maintainer: @magitian <magitian@duck.com>
pkgname=stratos-niri-config
pkgver=1.1
pkgrel=4
pkgdesc="Niri configuration for StratOS"
arch=('any')
license=('GPL3')
conflicts=('stratos-hyprland-config')
depends=(
	'bibata-cursor-theme-bin'
    'brightnessctl'
    'bluez-utils'
    'grim'
    'hyprpaper'
    'hypridle'
    'niri'
    'rofi-wayland'
    'slurp'
    'stratos-wallpapers'
    'stratos-waybar-niri-config'
    'swaync'
	'swayosd'
    'swappy'
    'ttf-jetbrains-mono'
    'ttf-jetbrains-mono-nerd'
    'wl-clipboard'
    'xdg-desktop-portal-gnome'
	'xorg-xwayland'
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
    install -d "$pkgdir/etc/skel/.config/niri"
    install -d "$pkgdir/etc/skel/.config/hypr"
    cp -r $srcdir/.config/niri/* $pkgdir/etc/skel/.config/niri/
    cp -r $srcdir/.config/hypr/* $pkgdir/etc/skel/.config/hypr/
}
