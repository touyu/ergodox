# ergodox-ez keymap

## Install Build Tools
https://docs.qmk.fm/#/getting_started_build_tools?id=macos

## ErgodoxEZ Configure
https://configure.ergodox-ez.com/tags?utf8=%E2%9C%93&q=touyu

Download Source code.

### Fix Source Code

コンパイルエラーになるので一部書き換える必要がある。
https://github.com/qmk/qmk_firmware/issues/3251
```
KEYMAP -> LAYOUT_ergodox
```

Commandで英かなを切り替えるため一部書き換え
```
GUI_T(KC_NO) -> GUI_T(KC_LANG2)
RGUI_T(KC_NO) -> RGUI_T(KC_LANG1)
```

## Compiling
```
git clone git@github.com:qmk/qmk_firmware.git
cd qmk_firmware
make git-submodule
```

keymap.cを`keyboards/ergodox_ez/keymaps/touyu/`に入れる

``` 
make keyboard=ergodox_ez  keymap=touyu
```
