# bitbake-recipe
Yocto bitbake tool to find recipes that provide a given package (real/virtual)

# Setup
Copy the `bitbake-recipe` file under `poky/bitbake/bin` and source the build environment again

# Test

This is tested on a layer meta-talel with recipe called "talel" that has 2 versions: 0.1 and 0.2

```sh
bitbake-recipe -p talel
| PN                             | PV     | PR | NATIVE? | PATH |
| ------------------------------ | ------ | -- | ------- | ---- |
| talel                          | 0.1    | r0 | No      | /path/to/meta-talel/recipes-example/example/talel_0.1.bb |
| talel                          | 0.2    | r0 | No      | /path/to/meta-talel/recipes-example/example/talel_0.2.bb |
```
