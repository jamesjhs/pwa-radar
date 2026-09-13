# pwa-radar
PWA-based 2D live radar simulator using OpenSky Network ADS-B data




## Development Phase Plan

### Phase 1: Discovery and Scope Definition
1. Define the primary user roles (e.g., enthusiast, analyst, educator).
2. Confirm v1 use-cases for 2D live aircraft tracking only.
3. Identify required public data sources and their access constraints.
4. Establish non-functional goals (performance, offline behavior, security, accessibility).

### Phase 2: Product and Technical Design
1. Draft user flows for core tasks (load map, ingest data, animate radar sweep, inspect targets).
2. Define architecture boundaries (frontend, data ingestion/adaptation, caching/offline layer).
3. Select rendering and mapping approach suitable for real-time browser visualization.
4. Produce a minimal domain model for tracks, detections, updates, and playback timeline.

### Phase 3: Foundation Setup
1. Initialize project structure and baseline coding standards.
2. Configure CI checks (lint, test, build) and branch protection expectations.
3. Set up environment configuration for local development and deployment.
4. Add baseline observability (error logging, performance metrics, health checks).

### Phase 4: Core Data Pipeline
1. Implement OpenSky Network API adapter and polling pipeline.
2. Normalize and validate inbound data into a consistent internal schema.
3. Add update scheduling/stream handling and resilience for partial data failures.
4. Introduce caching strategy for repeat queries and offline fallback behavior.

### Phase 5: Radar Simulation Engine
1. Implement track lifecycle logic (create, update, decay/remove).
2. Build radar sweep timing and interpolation for smooth movement.
3. Add filtering and prioritization rules (region, altitude, speed, source quality).
4. Validate simulation behavior against known sample scenarios.

### Phase 6: PWA Experience
1. Configure service worker for app shell caching and offline support.
2. Provide installable PWA manifest and cross-device compatibility checks.
3. Implement responsive UI for desktop/tablet/mobile with accessible controls.
4. Ensure degraded-but-usable mode during low connectivity.

### Phase 7: Quality, Security, and Hardening
1. Expand automated test coverage for data adapters, simulation logic, and UI flows.
2. Perform security checks on data handling, dependency risk, and client-side storage usage.
3. Run performance profiling for render loop and data update frequency.
4. Resolve bottlenecks and stabilize error recovery behaviors.

### Phase 8: Release and Iteration
1. Define release criteria and a staged rollout approach.
2. Prepare user-facing documentation and operational runbook.
3. Collect telemetry and user feedback after release.
4. Prioritize post-release improvements for the next iteration cycle.

## Finalized v1 Scope

1. Data source: OpenSky Network only.
2. Visualization: 2D radar display only.
3. Tracking mode: live tracking only (no historical playback in v1).
4. Deployment target: self-hosted within a web host.
5. Security/compliance: normal web best practices.
