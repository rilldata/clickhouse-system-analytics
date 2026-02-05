# Clickhouse System Analytics

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

Interactive dashboards for monitoring ClickHouse clusters via Rill.

## Table of Contents

- [Overview](#overview)
- [Quick Start](#quick-start)
- [Configuration](#configuration)
- [Deployment](#deployment)
- [Suggestions & Roadmap](#suggestions--roadmap)
- [Contributing](#contributing)
- [Support](#support)
- [License](#license)

## Overview

`clickhouse-system-analytics` provides dashboards to monitor the health and performance of your ClickHouse cluster. Powered by Rill, visualize:

- **Query Log**: Query metrics, latency percentiles, error rates, resource utilization.
- **Parts**: Storage health, compression ratios, merge levels, part distribution.
- **Part Log**: Merge operations, mutations, ZooKeeper activity.

## Quick Start

### Prerequisites

- Running ClickHouse cluster with network access.
- Rill CLI installed (`curl https://rill.sh | sh`).

### Clone

```bash
git clone https://github.com/rilldata/clickhouse-system-analytics.git
cd clickhouse-system-analytics
```

### Configure Credentials

```bash
cp .env.example .env
# Update CLICKHOUSE_HOST, CLICKHOUSE_PORT, CLICKHOUSE_USER, CLICKHOUSE_PASSWORD, CLICKHOUSE_CLUSTER
```

### Start Rill

```bash
rill start
```

Open http://localhost:9009

## Configuration

- Update `connectors/clickhouse.yaml` for connection settings.
- Modify SQL models in `models/` to adjust fields or filters.
- Tweak dimensions/measures in `metrics/`.
- Customize dashboards in `dashboards/`.

## Deployment

```bash
rill deploy
```

Refer to https://docs.rilldata.com/ for Rill Cloud details.

## Contributing

Contributions welcome! Please open issues or submit pull requests.

## Support

Report issues or request features: https://docs.rilldata.com/contact 

## License

Apache License 2.0. See [LICENSE](LICENSE).
