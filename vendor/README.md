# Ohm recovery dependency

`ohm-js-17.5.0-fallible.tgz` is built directly from
[Ohm PR #25](https://github.com/DavidSouther/ohm/pull/25) at
`b705247539a064fa2cb6edacab1980e060ba8740` (`split/fallible-docs`).
The complete upstream stack supplies recovery reuse, `Node.recoveredFailures`,
the three semantic slots of `B ! C`, and the `Failure#isLexical` metadata
used to distinguish lexical and parse diagnostics. No downstream patches
or sibling checkout are required.

The package retains upstream version `17.5.0`; this SHA-256 and the lockfile
integrity identify the unreleased build.

SHA-256: `6f2dd43db8c5ee3f496e8335227d960e463326504ea7a8e9b7ded858bf28ae2b`.

The archive was produced with `npm pack` from `packages/ohm-js` in a clean
checkout of the commit above. Its prepack hook builds the runtime and generates
declarations. The root `ohm-js` override keeps all workspaces on the same runtime
and declarations. Replace this artifact and its lockfile entry together when
changing Ohm.
