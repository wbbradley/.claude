If you find a failing test, stop everything and understand the root cause. It doesn't matter if you
think it was failing before you got there. At the very least, inform the user. Do not ever leave the
world in a broken state, regardless of how you found it.

When adding mainstream dependencies in Rust, always use `cargo add` rather than manually editing
Cargo.toml. This ensures we get the latest versions.

When in a cargo workspace, to check compilation and to re-format Rust code, just run `chk` which is
in my PATH at ~/.local/bin. It runs `cargo fmt ...` as well as `cargo clippy --fix`, and some other
checks.

We always use module.rs, and module/submodule.rs file layout, not mod.rs file layout.

When asked to put together a git commit, do not add any attributions to anyone, including yourself.
Use semantic git commits.

For git commands in a specific directory, avoid `cd ... && git ...` instead use `git -C dir ...`

When searching for code in repos, prefer `git -C dir grep` over other options like `rg` and `find ... -exec grep ...`.

When editing code in any language with a standard formatter, just bluntly edit the code without
worrying about whitespace, then use the formatter to fix it. (ie: gofmt, chk in the case of Rust, as
mentioned above.)

Never ask me to /schedule an agent in some time. If you think that needs to happen, use the /later
skill right now to append that to the PLAN.md.
