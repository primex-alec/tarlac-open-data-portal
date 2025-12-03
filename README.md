# Tarlac Open Data Portal

The official open data portal of Tarlac Province, providing transparent access to government datasets for citizens, researchers, developers, and organizations.

## 🌟 Features

- **📊 Browse 287+ Datasets** - Access public datasets across 22 categories including education, health, agriculture, infrastructure, and governance
- **🗺️ Interactive Maps** - Explore GIS data with interactive map layers for schools, hospitals, flood zones, and infrastructure
- **🔌 Developer API** - RESTful API with JSON, CSV, GeoJSON, and XLSX format support
- **🔍 Advanced Search** - Filter datasets by category, publisher, format, and keywords
- **📈 Data Visualizations** - Interactive charts and statistics for key provincial indicators
- **📱 Responsive Design** - Optimized for desktop, tablet, and mobile devices
- **♿ Accessible** - WCAG 2.1 compliant with keyboard navigation and screen reader support

## 🚀 Tech Stack

- **Framework:** [Next.js 15](https://nextjs.org/) with App Router
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **UI Components:** [shadcn/ui](https://ui.shadcn.com/)
- **Maps:** [Leaflet](https://leafletjs.com/) with [react-leaflet](https://react-leaflet.js.org/)
- **Charts:** [Recharts](https://recharts.org/)
- **Package Manager:** [pnpm](https://pnpm.io/)
- **Deployment:** [Vercel](https://vercel.com/)

## 📁 Project Structure

```
tarlac-open-data-portal/
├── app/                        # Next.js App Router pages
│   ├── about/                  # About page
│   ├── api-docs/              # API documentation
│   ├── categories/            # Categories listing and detail
│   ├── contribute/            # Contribution page
│   ├── datasets/              # Datasets listing and detail
│   ├── map/                   # Interactive map page
│   ├── maps/                  # Maps listing and detail
│   ├── layout.tsx             # Root layout
│   └── page.tsx               # Homepage
├── components/                 # React components
│   ├── map/                   # Map-specific components
│   ├── ui/                    # shadcn/ui components
│   ├── categories-grid.tsx    # Categories display
│   ├── dataset-card.tsx       # Dataset card component
│   ├── footer.tsx             # Site footer
│   ├── header.tsx             # Site header
│   └── ...                    # Other components
├── lib/                       # Utility functions and data
│   ├── data.ts               # Mock dataset data
│   ├── maps-data.ts          # Map layers data
│   └── utils.ts              # Helper functions
├── public/                    # Static assets
├── styles/                    # Global styles
│   └── globals.css
└── next.config.mjs           # Next.js configuration
```

## 🛠️ Getting Started

### Prerequisites

- Node.js 18+ and pnpm installed
- Git for version control

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/primex-alec/tarlac-open-data-portal.git
cd tarlac-open-data-portal
```

2. **Install dependencies**

```bash
pnpm install
```

3. **Run the development server**

```bash
pnpm dev
```

4. **Open your browser**

Navigate to [http://localhost:3000](http://localhost:3000)

### Build for Production

```bash
pnpm build
pnpm start
```

## 📄 Key Pages

- **Homepage** (`/`) - Featured datasets, statistics, and categories overview
- **Datasets** (`/datasets`) - Browse and search all available datasets
- **Dataset Detail** (`/datasets/[id]`) - View dataset details, resources, and metadata
- **Categories** (`/categories`) - Explore all 22 data categories
- **Category Detail** (`/categories/[id]`) - View datasets within a specific category
- **Interactive Map** (`/map`) - Explore map layers with schools, hospitals, and infrastructure
- **Maps Gallery** (`/maps`) - Browse available map layers
- **Map Detail** (`/maps/[id]`) - View individual map layer details
- **API Documentation** (`/api-docs`) - Developer API reference and examples
- **About** (`/about`) - Mission, vision, and contact information
- **Contribute** (`/contribute`) - Submit datasets and feedback

## 🗺️ Map Features

The interactive map (`/map`) includes:

- **Layer Controls** - Toggle schools, hospitals, infrastructure, flood zones, and landslide areas
- **GeoJSON Support** - Load custom GeoJSON data for flood and landslide zones
- **Marker Clustering** - Automatic grouping of nearby markers
- **Export Options** - Download map data in GeoJSON, Shapefile, and KML formats
- **Responsive Layout** - Split-panel design with resizable sidebar

## 🔌 API Endpoints (Mock)

The portal documentation describes the following API structure:

```
GET /api/v1/datasets              # List all datasets
GET /api/v1/datasets/{id}         # Get dataset by ID
GET /api/v1/datasets/{id}/resources  # List dataset resources
GET /api/v1/categories            # List all categories
GET /api/v1/publishers            # List all publishers
GET /api/v1/geojson/{layer}       # Get GeoJSON map data
```

## 🎨 Customization

### Theming

The portal uses CSS variables for theming. Modify `app/globals.css` to change colors:

```css
:root {
  --primary: 142 76% 36%;        /* Tarlac Green */
  --primary-foreground: 0 0% 98%;
  /* ... other variables */
}
```

### Data Sources

Update dataset information in:
- `lib/data.ts` - Categories, datasets, and statistics
- `lib/maps-data.ts` - Map layers and GIS datasets

## 📊 Key Components

### Main Components

- `MapComponent` - Leaflet map with layer controls
- `DatasetCard` - Dataset display card
- `CategoriesGrid` - Category tiles with icons
- `Header` - Site navigation and mobile menu
- `Footer` - Site footer with links and contact info

### UI Components

All UI components are from [shadcn/ui](https://ui.shadcn.com/) and located in `components/ui`:

- Button, Card, Badge, Input, Checkbox, Select, Dialog, etc.
- Fully customizable and accessible

## 🚢 Deployment

### Vercel (Recommended)

1. Push your code to GitHub
2. Import the repository in [Vercel](https://vercel.com)
3. Deploy with default Next.js settings

### Other Platforms

The app is a standard Next.js application and can be deployed to:
- Netlify
- AWS Amplify
- Google Cloud Run
- Any Node.js hosting platform

## 📝 License

This project is in the **public domain** under the Open Data Commons license. All content may be freely used, copied, distributed, and modified without permission, though attribution is appreciated.

## 🤝 Contributing

Contributions are welcome! Please see the Contribute page for guidelines on:

- Submitting datasets
- Reporting issues
- Suggesting features
- Improving documentation

## 📧 Contact

**Provincial Government of Tarlac**  
Provincial Capitol, Tarlac City, Tarlac 2300  
📞 (045) 982-0000  
📧 opendata@tarlac.gov.ph

## 🔗 Related Links

- [Provincial Government of Tarlac](https://tarlac.gov.ph)
- [Freedom of Information Portal](https://foi.gov.ph)
- [Philippine Statistics Authority](https://psa.gov.ph)
- [Open Data Philippines](https://data.gov.ph)

---

**Built with ❤️ for transparency and open government**
