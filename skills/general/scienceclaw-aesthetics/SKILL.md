# ScienceClaw Aesthetics — Publication-Quality Figure Standards

Rachel's aesthetic reference for all visualization work. Use this skill when generating any scientific figure.

---

## Color Palettes

### Scientific Journal Palettes (discrete, 2-10 groups)

| Name | Colors | Use for |
|------|--------|---------|
| **NPG** | `#E64B35` `#4DBBD5` `#00A087` `#3C5488` `#F39B7F` `#8491B4` `#91D1C2` `#DC0000` `#7E6148` `#B09C85` | Nature Publishing Group style |
| **Lancet** | `#00468B` `#ED0000` `#42B540` `#0099B4` `#925E9F` `#FDAF91` `#AD002A` `#ADB6B6` `#1B1919` | The Lancet style |
| **JCO** | `#0073C2` `#EFC000` `#868686` `#CD534C` `#7AA6DC` `#003C67` `#8F7700` `#3B3B3B` `#A73030` `#4A6990` | J Clinical Oncology |
| **NEJM** | `#BC3C29` `#0072B5` `#E18727` `#20854E` `#7876B1` `#6F99AD` `#FFDC91` `#EE4C97` | New England J Med |
| **AAAS** | `#3B4992` `#EE0000` `#008B45` `#631879` `#008280` `#BB0021` `#5F559B` `#A20056` `#808180` `#1B1919` | Science/AAAS |

### Qualitative Palettes (6-12 groups)

| Name | Colors |
|------|--------|
| **Paired** | `#A6CEE3` `#1F78B4` `#B2DF8A` `#33A02C` `#FB9A99` `#E31A1C` `#FDBF6F` `#FF7F00` `#CAB2D6` `#6A3D9A` `#FFFF99` `#B15928` |
| **Set1** | `#E41A1C` `#377EB8` `#4DAF4A` `#984EA3` `#FF7F00` `#FFFF33` `#A65628` `#F781BF` `#999999` |
| **Dark2** | `#1B9E77` `#D95F02` `#7570B3` `#E7298A` `#66A61E` `#E6AB02` `#A6761D` `#666666` |

### Continuous & Diverging

| Type | Options |
|------|---------|
| Sequential | `viridis`, `magma`, `plasma` |
| Diverging | `RdBu`, `Spectral`, `RdYlBu` |

### Special Purpose

| Name | Colors | Use |
|------|--------|-----|
| **Up/Down/NS** | Up: `#E64B35`, Down: `#4DBBD5`, NS: `#999999` | Volcano plots, differential expression |

### Selection Guide

- 2-5 groups: NPG or Lancet
- 6-12 groups: Paired
- 12+ groups: `colorRampPalette` interpolation
- Continuous data: viridis (sequential), RdBu (diverging)

---

## Journal Figure Sizing

| Preset | Width | Height | Base Font | DPI | Typical Use |
|--------|-------|--------|-----------|-----|-------------|
| `single_column` | 8.5 cm | 7 cm | 11 pt | 300 | Most journal figures |
| `one_half_column` | 12 cm | 9 cm | 12 pt | 300 | Medium-width figures |
| `double_column` | 17.5 cm | 10 cm | 13 pt | 300 | Full-width figures |
| `ppt` | 25 cm | 18 cm | 16 pt | 150 | Presentations |

---

## Aesthetic Rules

1. **Theme**: Clean and minimal. Start from `theme_classic()` (R) or equivalent. No unnecessary gridlines.
2. **Font**: Consistent sizing at `base_size` for the chosen preset. Helvetica or Arial preferred.
3. **Whitespace**: Generous margins. Elements should breathe.
4. **Color**: Every color must carry meaning. No decorative colors. No rainbow gradients unless data is continuous.
5. **Accessibility**: Always offer colorblind-safe alternatives. Never rely on color alone.
6. **Parameters at top**: All adjustable values (colors, sizes, paths) as variables at the top of the script.
7. **Return plot object**: Last expression returns the plot for further composition.
8. **Output formats**: PNG (300+ dpi), PDF (vector), SVG, TIFF. Always journal-spec compliant.
9. **3-second rule**: Reader should grasp the core message within 3 seconds.
10. **Consistency**: Within a project, all figures share the same visual language.
