# cace-action

GitHub composite action for CACE.

Insert the composite action into a workflow to set up the environment (PDK and tools) for CACE and execute it inside your repository:

```
...
      - name: Setup Environment and Run CACE
        uses: efabless/cace-action@latest
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
...
```

The following inputs are provided to customize the action:

```
...
      - name: Setup Environment and Run CACE
        uses: efabless/cace-action@latest
        with:
          pdk_family: 'sky130'
          open_pdks_rev: '4d5af10bfee4dab799566aaf903bb22aee69bac9'
          cace_rev: '4d5af10bfee4dab799566aaf903bb22aee69bac9'
          cace_root: '.'
          cace_datasheet: 'cace/ota-5t.yaml'
          cace_source: 'schematic'
          cace_args: '--summary summary.md'
          token: ${{ secrets.GITHUB_TOKEN }}
...
```

See `action.yml` for default values.