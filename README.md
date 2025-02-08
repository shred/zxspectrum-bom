# ZX Spectrum 48K Bill of Materials

This project contains the Bill of Materials for building an own **ZX Spectrum 48K Issue 3B** mainboard.

<div style="text-align:center;font-size:130%;font-weight:bold">
<a href="https://shred.codeberg.page/zxspectrum-bom/">Read the Bill of Materials here!</a>
</div>

## Contribute

This list is meant to be a community work. Our goal is to have a canonical list that people can rely on when ordering parts for building an own ZX Spectrum mainboard.

However, this list may not be free of errors. If you have found one, please [open an issue](https://codeberg.org/shred/zxspectrum-bom/issues) or send a patch.

## Technical Background

The main file of this project is the `zxspectrum-bom.yml` file. It contains the bill of material as YAML file, so it can be easily diffed by git and read by programs.

A Python tool called `generate.py` generates the website. You can find the generated web site in the `docs` directory. The converter needs these Python packages installed on your system:

* [PyYAML](https://pypi.org/project/PyYAML/)
* [Jinja2](https://pypi.org/project/Jinja2/)
* [jinja-markdown](https://pypi.org/project/jinja-markdown/)
* [XlsxWriter](https://pypi.org/project/XlsxWriter/)

## Disclaimer

This is not an official list! It was collected and reviewed by Sinclair enthusiasts.

Although we strive to make the information in this project as helpful and accurate as possible, it is provided "as is" and without warranties of any kind either expressed or implied. **Use it at your own risk!**

## Building

After cloning, initialize the submodule: `git submodule init; git submodule update`.

Invoke `generate.py` to generate the page content. You will find the generated pages in the `pages` directory.

## License

This project is distributed under the terms of [GNU General Public License (GPLv3)](https://www.gnu.org/licenses/gpl-3.0.en.html#content).
