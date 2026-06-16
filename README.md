# NF Milspec Premix Calculator — v1

National Foam Milspec Premix Calculator for nfmil.jonmercado.com.
Single-file, no build step, no dependencies.

---

## Deploy to Cloudflare Pages

1. Push this folder to a GitHub repo
2. Cloudflare dashboard → Workers & Pages → Create → Pages → Connect to Git
3. Build settings:
   - Framework preset: None
   - Build command: *(leave blank)*
   - Build output directory: `/` (root)
4. Set custom domain: `nfmil.jonmercado.com`

---

## Calculators

### Premix Calculator
- **Water (gal)** = Total Solution Mix × ((100 − %) / 100)
- **Foam (gal)**  = Total Solution Mix − Water (gal)
- **Water (lbs)** = Water (gal) × 8.345 lbs/gal
- **Water (kg)**  = Water (lbs) × 0.453592
- **Foam (lbs)**  = Foam (gal) × SG × 8.345 lbs/gal
- **Foam (kg)**   = Foam (lbs) × 0.453592
- **Volume (L)**  = gal × 3.785

Default Specific Gravity: 1.04

### EN Water Additive Calculator
Input water in gallons or lbs. Results in grams and lbs (4 decimal places).

| Additive             | Rate (g/gal) | Rate (g/lb) |
|----------------------|--------------|-------------|
| Magnesium Chloride (MgCl₂) | 0.1328 | 0.0159 |
| Calcium Chloride (CaCl₂)   | 0.3028 | 0.0363 |

Conversion: 1 lb = 453.592 g

---

## Version History

| Version | Notes           |
|---------|-----------------|
| v1      | Initial release                        |
| v2      | Updated water weight: 8.33 → 8.345 lbs/gal |
