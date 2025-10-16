# Portuguese Slave Marriage Records Collection

This digital collection presents historical manuscripts documenting slave marriages in 17th century Portugal. These ecclesiastical records, preserved in the Torre do Tombo National Archive, provide crucial insights into the social and legal frameworks surrounding slavery in early modern Portuguese society.

## Collection Overview

The collection consists of manuscript fragments from ecclesiastical records, specifically documenting slave marriages. These documents are organized into distinct collection groups:

- **PT-TT-CEL-002-544-1**: Contains 6 pages of marriage records
- **PT-TT-CEL-002-544-5**: Contains 9 pages of marriage records

Each collection represents different archival fragments from the same period, providing a comprehensive view of the marriage practices and legal frameworks of the time.

## Technical Implementation

This site is built using the WAX (Minimal Computing) framework, which provides:

- **Static site generation** for reliable, fast-loading pages
- **IIIF (International Image Interoperability Framework)** support for high-quality image viewing
- **Responsive design** that works across all devices
- **Search functionality** across collection metadata
- **Faceted browsing** by collection group, record type, and location

## Deployment Options

This site can be easily deployed to various platforms:

### GitHub Pages

1. Fork this repository
2. Enable GitHub Pages in repository settings
3. The site will automatically deploy via GitHub Actions

### Vercel

1. Connect your GitHub repository to Vercel
2. Vercel will automatically detect Jekyll and deploy
3. Custom domain can be configured in Vercel dashboard

### Netlify

1. Connect your GitHub repository to Netlify
2. Set build command: `bundle exec jekyll build`
3. Set publish directory: `_site`
4. Deploy automatically on push

## Local Development

To run this site locally:

```bash
# Install dependencies
bundle install

# Serve the site locally
bundle exec jekyll serve

# Build the site
bundle exec jekyll build
```

## Collection Structure

The collection is organized as follows:

- `_portugal/`: Individual markdown files for each collection item
- `_data/portugal.csv`: Metadata for all collection items
- `_data/raw_images/portugal/`: Original image files
- `_exhibits/`: Exhibit pages providing historical context
- `pages/`: Site pages (About, Collection, Search, etc.)

## Research Value

These records are invaluable for understanding:

- The legal status of enslaved individuals in Portuguese society
- Ecclesiastical involvement in colonial administration
- Social dynamics and family structures among enslaved populations
- Historical handwriting and bureaucratic practices of the period

## Acknowledgments

This collection is made possible through the cooperation of the Torre do Tombo National Archive and the Portuguese National Archives. The digital presentation utilizes open-source technologies to ensure long-term accessibility and preservation of these important historical documents.

## License

This collection is made available for educational and research purposes. Please refer to the original archival sources for specific usage rights and permissions.
