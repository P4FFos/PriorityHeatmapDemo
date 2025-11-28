# Priority Market Heatmap

Interactive single-page dashboard for exploring priority markets. It visualizes composite scores, filters, and market details for go-to-market planning.

## What You See
- **KPIs:** Top market, average score, and active region count.
- **Scatter chart:** Market size vs composite score; color by priority, highlight on selection.
- **Detail view:** Radar profile, channel strategy bars, metrics, search trend sparkline, and partner revenue hints.
- **Quick guide legend:** Interaction tips and priority color keys.

## Data Model
Markets live in `rawData` inside `index.html`. Each entry looks like:
```js
{
  id: "nyc",
  name: "New York",
  country: "USA",
  region: "North America",
  priority: "Top",          // Top | Medium | Low
  diaspora: 92,             // %
  recipe: 82,               // %
  social: 79,               // %
  trend: [48, ...],         // weekly search scores
  partners: ["Eataly", ...],
  opportunities: [...],
  channels: { retail: 36, ecom: 28, inf: 21, hosp: 15 },
  storeDensity: "High",
  internalDemand: 85,       // /100
  marketSize: 12,           // $M
  saturation: 60            // %
}
```

