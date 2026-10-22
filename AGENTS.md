# NARK: notes for agents

- **Notation comes from the Econ-ARK notation registry.** Read
  `@resources/notation/NOTATION.md` before changing a symbol in `NARK.tex`. The registry is
  maintained in `econ-ark/econ-ark-tools`; a change to a symbol is made there, not here.
- **`@resources/` is a read-only copy.** Refresh it with
  `./@resources-update-from-remote_private.sh`, which leaves it read-only (`chmod -R u-w`).
  A git checkout, merge or rebase that changes a file under it therefore stops partway with
  "Permission denied": run `chmod -R u+w @resources` first and `chmod -R u-w @resources` after.
- **Build with `latexmk`.** `.latexmkrc` puts `@resources/texlive/texmf-local` ahead of the
  system's TeX tree, so the build uses this repo's econark files. Build the committed `NARK.pdf`
  where cm-super is installed: `pdffonts NARK.pdf` should list no Type 3 fonts.
