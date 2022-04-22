# Ayaka PKGBUILD Repository

Provide PKGBUILDs maintained by Ayaka

## List

| Name | Description | Version | Last Updated |
| :- | :- | :- | :- |
| grain | A modern web staple. A new language that puts academic language features to work | 0.4.7-1 | 2022-01-18 |
| rime-ipa | IPA input for rime | 0.0.0.20200413-1 | 2020-07-25 |
| rime-nushu | Nushu input for rime | 0.0.0.20200722-2 | 2021-08-14 |
| rime-symbolic | Symbolic input for rime | 0.0.0.20200813-1 | 2020-08-16 |
| rime-symbolic-simp | Symbolic input for rime (Simplified Chinese version) | 0.0.0.20200813-1 | 2020-08-16 |
| rime-tupa | TUPA input for rime | 0.0.0.20220422-1 | 2022-04-22 |
| ttf-fanwunming | A Simplified-Chinese-to-Traditional-Chinese font based on GenYoMin, which can handle the one-to-many problem | 1.007-1 | 2021-09-08 |
| ttf-fanwunhak | A Simplified-Chinese-to-Traditional-Chinese font based on GenYoGothic, which can handle the one-to-many problem | 1.007-1 | 2021-09-08 |

## Workflow

```sh
cd $packagename
makepkg -g >> PKGBUILD
makepkg --printsrcinfo > .SRCINFO
makepkg -s
namcap *.tar.zst
sudo pacman -U *.tar.zst
git add PKGBUILD .SRCINFO
git add ../README.md
git commit -m "Add $packagename"
aurpublish $packagename
git push
git clean -xdf
```

## Thanks

- **[ayalhw/AUR](https://github.com/ayalhw/AUR)**: Great AUR repository
- **[aurpublish](https://github.com/eli-schwartz/aurpublish)**: Great tool to manager your AUR PKGBUILDs
- **[nvchecker](https://github.com/lilydjwg/nvchecker)**: Great tool to check newer version of packages
