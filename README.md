# kzntsv-dev Claude Code Plugins

A marketplace catalog of Claude Code plugins by
[Victor Kuznetsov](https://github.com/kzntsv-dev).

## Adding this marketplace

Run once per machine in Claude Code:

```
/plugin marketplace add kzntsv-dev/claude-plugins
```

After that, individual plugins can be installed by name:

```
/plugin install <plugin-name>@opeitcloc03-claude-plugins
```

## Available plugins

### [yt-tools](https://github.com/kzntsv-dev/yt-tools)

CLI suite for iterative agent-driven YouTube watching: clean-markdown
transcripts with `[mm:ss]` anchors, targeted frame extraction, and FFT audio
analysis (BPM, key, chord progression, spectral statistics). Bundles the
`using-yt-tools` skill that orchestrates three primary flows (iterative watch
/ targeted frames / audio analysis).

Install:

```
/plugin install yt-tools@opeitcloc03-claude-plugins
```

The plugin's `SessionStart` hook auto-runs
`pipx install --force "$CLAUDE_PLUGIN_ROOT[full]"` (from the plugin's local
clone, with fallback to core if `[full]` extras fetch fails) and probes
`ffmpeg` on first session after install. External `ffmpeg` binary required —
the plugin will guide you through per-OS install if missing.

## Contributing

This marketplace serves plugins authored by `@kzntsv-dev`. Bug reports and
plugin-specific issues should be filed in the individual plugin repositories.

## License

Each plugin is independently licensed (see its repository). The
`marketplace.json` catalog itself is MIT — see [LICENSE](LICENSE).
