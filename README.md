# Corsair

![corsair_arch](https://raw.githubusercontent.com/esynr3z/corsair/master/docs/arch.svg)

Corsair is a tool that makes it easy to organize and support control and status register (CSR) map for any FPGA/ASIC project.
You just need to create and fill single CSR map description file once and then generate HDL code, headers, documentation and etc.

It is as easy as:

* Create CSR map description file or generate a template with Corsair:

```sh
corsair --template-regmap regs.json
```

* Make changes to ```regs.json```
* Generate output artifacts:

```sh
corsair -r regs.json --hdl --lb-bridge --docs
```

* You will get:
  * Register map HDL code
  * Bridge to some standart interface (e.g. AXI-Lite, depends on configuration)
  * Document, describing the map

For more details about ways the tool can be used and how it works please refer the documentation at [Read the docs](https://corsair.readthedocs.io).

## Installation

You can install the latest stable version from pypi:

```sh
python3 -m pip install -U corsair
```

## Development

Corsair is still under development. Please follow the [Developers Guide](https://corsair.readthedocs.io/en/latest/contributing.html).

## License

Corsair is licensed under [MIT License](LICENSE.txt).
