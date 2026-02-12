# Ayaka PKGBUILD Repository

PKGBUILD files maintained by Ayaka

## List

| Name | Description | Version | Last Updated |
| :- | :- | :- | :- |
| grain-bin | A modern web staple. A new language that puts academic language features to work | 0.5.13-1 | 2023-01-09 |
| rime-ipa | IPA input for rime | 0.0.0.20200413-1 | 2020-07-25 |
| rime-nushu | Nushu input for rime | 0.0.0.20200722-2 | 2021-08-14 |
| rime-symbolic | Symbolic input for rime | 0.0.0.20200813-1 | 2020-08-16 |
| rime-symbolic-simp | Symbolic input for rime (Simplified Chinese version) | 0.0.0.20200813-1 | 2020-08-16 |
| rime-tupa | TUPA input for rime | 0.0.0.20260212-1 | 2026-02-12 |
| ttf-fanwunming | A Simplified-Chinese-to-Traditional-Chinese font based on GenYoMin, which can handle the one-to-many problem | 1.007-1 | 2021-09-08 |
| ttf-fanwunhak | A Simplified-Chinese-to-Traditional-Chinese font based on GenYoGothic, which can handle the one-to-many problem | 1.007-1 | 2021-09-08 |

## Workflow

```sh
cd $packagename
# <Edit PKGBUILD, and comment out `sha256sums`>
makepkg -g >> PKGBUILD
# <Edit PKGBUILD, substitute the commented `sha256sums` to the newly generated one>
makepkg --printsrcinfo > .SRCINFO
makepkg -s
namcap *.pkg.tar
sudo pacman -U *.pkg.tar
git add PKGBUILD .SRCINFO
# <Edit README.md, update the "Last Updated" field>
git add ../README.md
git commit -m "Update $packagename"
aurpublish $packagename
git push
git clean -xdf
```

## Thanks

- **[ayalhw/AUR](https://github.com/ayalhw/AUR)**: Great AUR repository
- **[aurpublish](https://github.com/eli-schwartz/aurpublish)**: Great tool to manager your AUR PKGBUILDs
- **[nvchecker](https://github.com/lilydjwg/nvchecker)**: Great tool to check newer version of packages
