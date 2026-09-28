# astli-pre-commit

A [pre-commit](https://pre-commit.com) hook for
[astli](https://github.com/fischeti/astli), the SystemVerilog formatter.

```yaml
repos:
  - repo: https://github.com/fischeti/astli-pre-commit
    rev: v0.2.0
    hooks:
      - id: astli-fmt
```

`astli-fmt` rewrites `.sv`, `.svh`, `.v` and `.vh` files in place. To limit it
to SystemVerilog, add `types_or: [system-verilog]` to the hook.

Each tag installs the astli release of the same version from PyPI, so `rev`
picks the formatter, and `pre-commit autoupdate` upgrades it. Tags follow astli
releases within a day.

## License

Licensed under either of [Apache License, Version 2.0](LICENSE-APACHE) or
[MIT license](LICENSE-MIT) at your option.
