# PRD: Product Usage Analytics

## 1) Business Context
- Goal: Measure adoption + engagement, identify product opportunities
- Consumers: Product, Growth, Data Analysts

## 2) Vulcan-First Specification
- Grain: customer_id x component_id x day
- Entities: customer_id, component_id, feature_id
- Primary time: event_timestamp (UTC)
- Dimensions: customer_segment, region
- Measures: views, clicks, installations
- Metrics: CTR, views_per_customer, installation_rate

## 3) Sources
- (fill later)

## 4) Freshness & Backfill
- Cadence: daily
- Backfill: 90 days

## 5) Open Questions
- DQ checks, PII, output dataset names
