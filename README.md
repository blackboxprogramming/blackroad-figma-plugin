# 🌌 BlackRoad Brand System - Figma Plugin

**Official brand standards directly in Figma**

Version: 2.0.0
Platform: Figma & FigJam
Status: ✅ Ready to Install

---

## 🎯 Features

### Brand Colors
- ✅ All 10 brand colors with exact hex values
- ✅ One-click apply to selection
- ✅ Visual color swatches
- ✅ Primary colors marked with ★

### Brand Gradient
- ✅ 135° gradient with Golden Ratio stops
- ✅ Stops at 0%, 38.2%, 61.8%, 100%
- ✅ One-click apply to selection
- ✅ Visual gradient preview

### Spacing System
- ✅ Fibonacci sequence (8, 13, 21, 34, 55, 89, 144)
- ✅ Visual spacing bars
- ✅ Golden Ratio based

### Quick Actions
- ✅ Create color palette frame
- ✅ Create spacing guide frame
- ✅ Create BlackRoad logo
- ✅ Create full component library

---

## 📦 Installation

### Method 1: Import to Figma

1. **Open Figma Desktop App**

2. **Go to Plugins Menu**:
   - Menu → Plugins → Development → Import plugin from manifest

3. **Select Manifest**:
   - Navigate to `/tmp/blackroad-brand-figma-plugin/`
   - Select `manifest.json`

4. **Plugin Installed!**
   - Now available in: Plugins → Development → BlackRoad Brand System

### Method 2: Manual Setup

1. **Copy Plugin Files**:
   ```bash
   # Create Figma plugin directory
   mkdir -p ~/figma-plugins/blackroad-brand-system

   # Copy files
   cp /tmp/blackroad-brand-figma-plugin/* ~/figma-plugins/blackroad-brand-system/
   ```

2. **Import in Figma**:
   - Figma → Plugins → Development → Import plugin from manifest
   - Select: `~/figma-plugins/blackroad-brand-system/manifest.json`

---

## 🚀 Usage

### Applying Brand Colors

1. **Select an object** in Figma (rectangle, frame, text, etc.)
2. **Run plugin**: Plugins → Development → BlackRoad Brand System
3. **Click any color** in the color grid
4. ✅ Color applied instantly!

**Primary Colors** (marked with ★):
- Hot Pink (#FF1D6C)
- Amber (#F5A623)
- Electric Blue (#2979FF)
- Violet (#9C27B0)

**Secondary Colors**:
- Black (#000000)
- White (#FFFFFF)
- Orange (#F26522)
- Magenta (#E91E63)
- Sky Blue (#448AFF)
- Deep Purple (#5E35B1)

### Applying Brand Gradient

1. **Select an object**
2. **Run plugin**
3. **Click "Apply to Selection"** under Brand Gradient section
4. ✅ Gradient applied with Golden Ratio stops!

**Gradient Details**:
- Angle: 135°
- Stops: 0% (Amber), 38.2% (Hot Pink), 61.8% (Violet), 100% (Electric Blue)
- Golden Ratio positions: 38.2% and 61.8% (φ = 1.618)

### Creating Brand Assets

#### Color Palette Frame
```
1. Click "Create Color Palette"
2. Full-page color swatch board created
3. All primary colors with names and hex values
4. Ready to use as reference
```

#### Spacing Guide Frame
```
1. Click "Create Spacing Guide"
2. Visual spacing scale created
3. Shows all Fibonacci values (8-144px)
4. Each spacing value with visual bar
```

#### BlackRoad Logo
```
1. Click "Create BlackRoad Logo"
2. Official logo created as frame
3. Hot pink circle border
4. Amber top half, electric blue bottom
5. Black center circle
6. Ready to use or copy
```

#### Full Component Library
```
1. Click "Create Full Library"
2. New page created
3. Sections for colors, spacing, logo
4. Complete brand system reference
```

---

## 📐 Spacing System

All spacing follows the Golden Ratio (φ = 1.618) using Fibonacci sequence:

```
--space-xs:  8px   (Fibonacci F6)
--space-sm:  13px  (Fibonacci F7)
--space-md:  21px  (Fibonacci F8)
--space-lg:  34px  (Fibonacci F9)
--space-xl:  55px  (Fibonacci F10)
--space-2xl: 89px  (Fibonacci F11)
--space-3xl: 144px (Fibonacci F12)
```

**Usage in Figma**:
- Use these exact values for padding, margins, gaps
- Creates harmonious, mathematically balanced designs
- Consistent with all BlackRoad projects

---

## 🎨 Brand Colors Reference

### Primary Colors

| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Hot Pink | #FF1D6C | 255, 29, 108 | Primary brand color |
| Amber | #F5A623 | 245, 166, 35 | Gradient start |
| Electric Blue | #2979FF | 41, 121, 255 | Gradient end |
| Violet | #9C27B0 | 156, 39, 176 | Gradient middle |

### Supporting Colors

| Color | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Black | #000000 | 0, 0, 0 | Backgrounds |
| White | #FFFFFF | 255, 255, 255 | Text, highlights |
| Orange | #F26522 | 242, 101, 34 | Accents |
| Magenta | #E91E63 | 233, 30, 99 | Accents |
| Sky Blue | #448AFF | 68, 138, 255 | Accents |
| Deep Purple | #5E35B1 | 94, 53, 177 | Accents |

---

## 🔧 Technical Details

### Files

```
blackroad-brand-figma-plugin/
├── manifest.json       # Plugin configuration
├── code.js            # Plugin logic (Figma API)
├── ui.html            # Plugin UI (400x600)
└── README.md          # This file
```

### Plugin API

**Messages from UI to Code**:
- `apply-color` - Apply color to selection
- `create-gradient` - Apply gradient to selection
- `create-color-palette` - Create color palette frame
- `create-spacing-guide` - Create spacing guide frame
- `create-logo` - Create BlackRoad logo
- `create-component-library` - Create full library page

**Figma API Usage**:
- `figma.createFrame()` - Create frames for palettes/guides
- `figma.createRectangle()` - Create color swatches
- `figma.createEllipse()` - Create logo circles
- `figma.createText()` - Create labels
- `node.fills` - Apply colors/gradients
- `figma.notify()` - Show success messages

---

## 🎓 Workflow Examples

### Example 1: Designing a Landing Page

```
1. Open Figma, create new file
2. Run BlackRoad Brand System plugin
3. Click "Create Color Palette" (for reference)
4. Create your design frames
5. Use plugin to apply colors as you design
6. Use spacing guide for consistent padding/margins
7. Add BlackRoad logo from plugin
8. Export design
9. Implement with exact same colors/spacing in code
```

### Example 2: Creating Marketing Materials

```
1. Create artboard in Figma
2. Run plugin
3. Apply brand gradient to background
4. Use Hot Pink for primary CTA buttons
5. Use Amber for highlights
6. Use --space-lg (34px) for padding
7. Add BlackRoad logo
8. Export as PNG/SVG
```

### Example 3: Building Design System

```
1. Run plugin
2. Click "Create Full Library"
3. New page created with all brand assets
4. Add your custom components
5. Use as team design system
6. Share with designers
7. Ensure brand consistency across all work
```

---

## ✅ Compliance Checking

The plugin ensures 100% brand compliance by:
- ✅ Using exact hex values (no approximations)
- ✅ Enforcing Golden Ratio spacing
- ✅ Correct gradient stops (38.2%, 61.8%)
- ✅ Official logo structure
- ✅ Consistent with all other brand tools

**Integration with Other Tools**:
- Export from Figma
- Check with browser extension
- Validate with CLI tool
- Deploy with enforcement scripts
- Monitor with dashboard

---

## 🚨 Common Issues

### Plugin not showing?
1. Make sure you're using Figma Desktop (not browser)
2. Check: Plugins → Development
3. Reimport manifest if needed

### Colors not applying?
1. Select an object first
2. Make sure object supports fills (not groups)
3. Check console for errors

### Text not working?
1. Figma requires font loading for text
2. Plugin uses "Inter" font (Figma default)
3. Make sure Inter is available

### Logo creation fails?
1. Check you have edit permissions
2. Try on a new page
3. Check console for errors

---

## 📊 Plugin Stats

- **10 brand colors** with exact hex values
- **7 spacing values** (Fibonacci sequence)
- **1 brand gradient** (Golden Ratio stops)
- **4 quick actions** for asset creation
- **100% brand compliance** guaranteed

---

## 🔗 Integration

### With Other Brand Tools

| Tool | Integration |
|------|-------------|
| Browser Extension | Design in Figma → Check in browser |
| CLI Tool | Export → Validate → Deploy |
| Audit Script | Ensure consistency |
| Dashboard | Monitor compliance |
| GitHub Actions | Automated checks |

### Workflow

```
Figma Plugin → Export Design
       ↓
Browser Extension → Check compliance
       ↓
CLI Tool → Validate code
       ↓
Deploy Tool → Push to production
       ↓
Dashboard → Monitor live site
```

---

## 🎉 Benefits

### For Designers
- ✅ Exact brand colors always available
- ✅ No manual color picking
- ✅ Consistent spacing automatically
- ✅ Quick asset creation
- ✅ No need to reference docs

### For Developers
- ✅ Design matches code exactly
- ✅ Same hex values in Figma and CSS
- ✅ Same spacing scale
- ✅ Easy handoff
- ✅ No surprises in implementation

### For Teams
- ✅ Brand consistency across all work
- ✅ No deviations or mistakes
- ✅ Fast onboarding for new designers
- ✅ Single source of truth
- ✅ Automated enforcement

---

## 📚 Resources

- **Brand System**: ~/BLACKROAD_BRAND_SYSTEM.md
- **CLI Tool**: @blackroad/brand-cli
- **Browser Extension**: /tmp/blackroad-brand-extension/
- **Website**: https://blackroad-os-brand.pages.dev
- **GitHub**: https://github.com/BlackRoad-OS

---

## 🔮 Future Enhancements

Potential future features:
- Component templates (buttons, cards, etc.)
- Typography scale with SF Pro Display
- Animation presets
- Export to code snippets
- Team library sync
- Version control integration

---

## 📝 Version History

### v2.0.0 (Current)
- ✅ Initial release
- ✅ 10 brand colors
- ✅ Brand gradient with Golden Ratio
- ✅ Fibonacci spacing scale
- ✅ Logo generator
- ✅ Quick actions for asset creation
- ✅ Full component library generator

---

## 📞 Support

- **Email**: blackroad.systems@gmail.com
- **GitHub**: https://github.com/BlackRoad-OS
- **Docs**: https://blackroad-os-brand.pages.dev

---

**NO MORE DEVIATIONS. BRAND COMPLIANCE STARTS IN DESIGN.**

🔒 LOCKED · 🎨 STANDARDIZED · 🚀 ENFORCED · 🤖 AUTOMATED

---

**Part of the complete BlackRoad Brand System**
© 2024 BlackRoad OS
