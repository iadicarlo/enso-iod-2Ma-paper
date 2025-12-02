## Fixing Colorbar Font-Size Mismatches

When you spot a plot whose axis labels use one font size but its colorbar label/ticks use another (like the issue we just fixed in `2_IOD_ENSO_mean_std.ipynb`), follow these steps:

1. **Locate the plotting cell**
   - Open the notebook (`2_IOD_ENSO_mean_std.ipynb` in our case) and find the cell(s) that build the figure with the inconsistent fonts.
   - Search for `colorbar(` to jump straight to relevant code.

2. **Capture the base font size**
   - After any `pplt.rc['font.size'] = ...` call, store the value in a helper variable so it can be reused consistently:
     ```python
     pplt.rc['font.size'] = 45
     base_fontsize = pplt.rc['font.size']
     ```

3. **Apply the shared size to each colorbar**
   - For standard Matplotlib colorbars:
     ```python
     cbar = ax.colorbar(...)
     cbar.set_label(..., fontsize=base_fontsize)
     cbar.ax.tick_params(labelsize=base_fontsize)
     ```
   - For ProPlot colorbars that use `colorbar_kw`, set both `labelsize` and `ticklabelsize` to `base_fontsize`.

4. **Repeat for every figure in the cell**
   - Some cells create multiple subplots or multiple figures—ensure each colorbar (including inset or shared bars) uses the same `base_fontsize`.

5. **Re-run the cell and verify**
   - Execute the modified cell to regenerate the figure.
   - Confirm axis labels, tick labels, and colorbar labels/ticks now match visually.

Following these steps keeps typography consistent across axes and colorbars whenever the issue reappears.

