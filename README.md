# tmux-load-avg

This is a `tmux` plugin that displays the system load average in the last 1, 5 and 15 minutes.

### Usage

Add `#{load_average}` format string to existing `status-right` tmux option.
Here's an example in `.tmux.conf`:

    set -g status-right "Load:#{load_average} | %a %h-%d %H:%M "

### Installation with [Tmux Plugin Manager](https://github.com/tmux-plugins/tpm) (recommended)

Add plugin to the list of TPM plugins in `.tmux.conf`:

    set -g @plugin 'dastergon/tmux-load-avg'

Hit `prefix + I` to fetch the plugin and source it.

If format strings are added to `status-right`, they should now be visible.

### Manual Installation

Clone the repo:

    $ git clone https://github.com/dastergon/tmux-load-avg ~/clone/path

Add this line to the bottom of `.tmux.conf`:

    run-shell ~/clone/path/load_average.tmux

Reload TMUX environment:

    # type this in terminal
    $ tmux source-file ~/.tmux.conf

If format strings are added to `status-right`, they should now be visible.

## Special Credit
This plugin is based on the various plugins in [tmux-plugins](https://github.com/tmux-plugins) Github page.
