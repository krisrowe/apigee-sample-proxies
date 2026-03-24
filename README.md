# Apigee Sample Proxies

This repository contains a set of sample proxies for validating Apigee Hybrid deployments.

## Proxy Options

1.  **`stubbed-backend`**:
    - **Basepath**: `/stub/v1`
    - **Description**: A targetless proxy that returns a hardcoded JSON response. Use this for smoke testing when no egress is allowed.
    - **Implementation**: Uses `AssignMessage` policy to return a fixed payload.

2.  **`weather-gov`**:
    - **Basepath**: `/weather/v1`
    - **Description**: Targets the public `api.weather.gov` API. Use this to verify public internet egress and TLS verification. [Confirmed targeting `api.weather.gov/stations`].

3.  **`gcp-backend`**:
    - **Basepath**: `/gcp/v1`
    - **Description**: Targets a sample backend on GCP (Placeholder IP: `35.241.211.133`). Use this to verify private/internal routing capabilities.

## Usage

Each folder is a standard Apigee bundle containing the `apiproxy` directory. They are "ready to deploy" for any Apigee Hybrid environment validation task.
