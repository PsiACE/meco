# Meco

> Some things are useless, but try them anyway.

Meco, a C project template with Meson.

It was created because I once blamed my poor C programming skills on the lack of a project template. :)

_**Note:**_ There is still a lot of work to do, but it is currently available.

## Usage

If you want to try it, consider installing the `meson` build system, and `ninja` must also be installed with it.
For example, on the fedora platform, run `dnf install meson`.

### Basic

```bash
git clone git@github.com:PsiACE/meco.git your-awesome-project
# or `git clone https://github.com/psiace/meco.git your-awesome-project`
cd your-awesome-project
```

Replace `meco` in all text with `your-awesome-project`. And then:

```bash
meson builddir
ninja -C builddir # -j8
meson install # for test, just run `./builddir/src/your-awesome-project`
```

Now it should be added to your system. You can run `your-awesome-project` in the terminal.

### Other

In addition, the three subcommands `release`, `format` and `run` are provided for easy use.

Just run `ninja -C builddir <subcommand>`.

Please modify scripts or files to carry out your custom activities.

_**Note:**_ Since the `format` script relies on `clang-format`, consider installing it.

## Contact

Chojan Shang - [@PsiACE](https://github.com/psiace) - <psiace@outlook.com>

Project Link: [https://github.com/psiace/meco](https://github.com/psiace/meco)

## License

- MIT license ([LICENSE](./LICENSE) or [http://opensource.org/licenses/MIT](http://opensource.org/licenses/MIT))
