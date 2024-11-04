# Documentation Common

This repository contains LaTeX formatting and common commands that we will use for all
documentation. Use this repository as a submodule to any documentation repository.

## References

Note that there is a [reference file](references.bib) in this repository. To use this
reference file in your documentation include the following command in you main LaTeX
file where you would like the bibliography to appear.

```latex
\bibliography{documentation-common/references.bib}
```

This command to add the reference file must be added if references are used. You may add as
many `.bib` files as commas-separated file paths inside the curly brackets of the above command.
Be aware that if there are redundant reference keys in the reference files used there
will not be any error or warning thrown. So if you are using more than one reference file
make sure that your reference file does not contain references with keys that are identical
to the ones in [references.bib](references.bib) in this repository.
