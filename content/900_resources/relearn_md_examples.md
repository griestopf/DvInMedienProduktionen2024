+++
title = "Relearn md examples"
date = 2024-08-05T14:20:54+02:00
draft = false 
weight = 9999
+++

In addition to the features offered by [GitHub-Flavored-Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), the [Hugo Relearn Theme](https://mcshelby.github.io/hugo-theme-relearn/i) allows the following extra features:

Press <kbd>STRG</kbd> <kbd>ALT</kbd> <kbd>DEL</kbd> to end your shift early.

How many liters H~2~O fit into 1dm^3^?

Double quotes `"` and single quotes `'` of enclosed text are replaced by **"double curly quotes"** and **'single curly quotes'**.

Double dashes `--` and triple dashes `---` are replaced by en-dash **--** and em-dash **---** entities.

Double arrows pointing left `<<` or right `>>` are replaced by arrow **<<** and **>>** entities.

Three consecutive dots `...` are replaced by an ellipsis **...** entity.

~~Strike through~~ this text

The ++hot, new++ stuff

==Parts== of this text ==are marked!==


[Font Awesome icons](https://fontawesome.com/icons) (only non-pro are supported): 
{{% icon icon="exclamation-triangle" %}}
{{% icon icon="angle-double-up" %}}
{{% icon icon="skull-crossbones" %}}
{{% icon icon=" gamepad" %}}

Inline math is generated if you use a single `$` as a delimiter around your formulae: {{< math >}}$\sqrt{3}${{< /math >}}

{{< math align="center" >}}
$$\left( \sum_{k=1}^n a_k b_k \right)^2 \leq \left( \sum_{k=1}^n a_k^2 \right) \left( \sum_{k=1}^n b_k^2 \right)$$
{{< /math >}}

