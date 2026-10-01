# E-Waste Compliance Tracker

`e-waste-compliance-tracker` provides a policy-driven evidence chain for electronics leaving repair and refurbishment operations, from classification and secure storage through approved downstream treatment and audited mass balance.

## Capabilities

- Priority-based waste-code, stream, hazard, and handling classification
- Inventory identity, positive mass, hazardous code, and data-sanitization validation
- Containment, lithium-battery isolation, access, capacity, and storage-time controls
- Downstream vendor certifications, streams, audit, geography, and insurance qualification
- Deterministic content-hashed shipment manifests
- Hazardous-carrier authorization and manifest-integrity checks
- Ordered holder chain of custody with evidence hashes
- Receipt item/mass reconciliation and tolerances
- Reuse, recycling, recovery, landfill, diversion, and mass-balance accounting
- Downstream certificates and duplicate detection
- Verified data-destruction coverage
- Program metrics, audit readiness, and Markdown reports
- Dependency-free Node.js 18+ library and CLI

## Quick start

```bash
npm install
npm test
node src/cli.js classify examples/item.json examples/rules.json
node src/cli.js inventory examples/items.json
node src/cli.js manifest examples/meta.json examples/items.json examples/vendor.json --output manifest.json
node src/cli.js validate-manifest manifest.json
```

## Library API

```js
import { classifyItem, vendorQualification, createManifest, custodyLedger, massBalance } from '@opencircuitlabs/e-waste-compliance-tracker';
```

The package intentionally contains no hard-coded legal claims. Organizations must configure current jurisdiction-specific waste codes, storage limits, transporter and downstream requirements, export restrictions, retention, and reporting with qualified environmental and legal review.

## License

MIT. See [LICENSE](LICENSE).
