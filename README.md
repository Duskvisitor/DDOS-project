
DDOS-project

# ddos-dmz-auto

A rapid prototype that detects DDoS attacks via API thresholds, spins up an isolated DMZ with Terraform, and reroutes traffic through the new perimeter.

## Features

- Threshold-based DDoS detection (Cloudflare/AWS metrics)  
- On-demand DMZ provisioning (Terraform VPC, subnet, SG)  
- Automated DNS/CDN traffic steering  
- Simple CLI orchestration

## Prerequisites

- Python 3.10+  
- Terraform 1.0+  
- Keycloak account with API credentials  
- Cloudflare or Route 53 API token

## Configuration

Create a `.env` in project root:
```dotenv
CF_API_TOKEN=your_cloudflare_token
AWS_ACCESS_KEY_ID=…
AWS_SECRET_ACCESS_KEY=…
THRESHOLD=10000
ZONE_ID=your_dns_zone_id
