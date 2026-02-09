# codex-qa
QA

## Resolving notebook conflicts
If you have conflicting versions of `pdf_to_base64.ipynb` (upload widget vs. local path), keep the local-path version and drop the older widget-based commit. The simplest options are:

- Use an interactive rebase to drop the older commit:
  - `git rebase -i <base>` and delete the widget commit line.
- While resolving a merge conflict, choose the local-path version:
  - `git checkout --ours pdf_to_base64.ipynb` then `git add pdf_to_base64.ipynb`.

This keeps the notebook aligned with the current requirement to use a local file path instead of an upload widget.
