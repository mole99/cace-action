# cace-action

GitHub composite action for CACE.

Insert the composite action into a workflow to set up the environment (PDK and tools) for CACE and execute it inside your repository:

```
...
      - name: Setup Environment and Run CACE
        uses: efabless/cace-action@main
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
...
```

The following inputs are provided to customize the action, for example:

```
...
      - name: Setup Environment and Run CACE
        uses: efabless/cace-action@main
        with:
          pdk_family: 'sky130'
          open_pdks_rev: '4d5af10bfee4dab799566aaf903bb22aee69bac9'
          cace_rev: '863badbdd7a0ab420421db09e59ba0e0e988ecdb'
          cace_root: '.'
          cace_datasheet: 'cace/ota-5t.yaml'
          cace_source: 'schematic'
          cace_args: '--log-level DEBUG'
          token: ${{ secrets.GITHUB_TOKEN }}
...
```

See `action.yml` for default values.
