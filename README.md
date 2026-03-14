# zakat

## Technical Overview

This application is a Zakat calculation and educational web application built with .NET 8 using Blazor WebAssembly. It provides both informational content about Zakat and interactive calculators that help users estimate their Zakat obligations across different types of assets. The application is designed as a client-side single-page application (SPA) that runs entirely in the browser using WebAssembly. This allows the app to deliver a fast and responsive experience without requiring server-side computation for Zakat calculations.

## Core Technologies

- .NET 8
- Blazor WebAssembly
- C#
- Razor Components
- HTML5 / CSS
- Client-side state management

## Application Architecture

The application follows a component-based architecture using Blazor Razor components. Each calculator and informational section is encapsulated in reusable UI components to promote maintainability and separation of concerns.

### Key architectural characteristics include:

- Client-side execution using WebAssembly
- Component-driven UI built with Razor components
- Strongly typed calculation logic implemented in C#
- Separation between UI, calculation logic, and data models
- Stateless calculation workflows for predictable results
- Functional Modules

### The application consists of two main functional areas:

1. Educational Content

The platform provides structured educational material covering:

- Historical background of Zakat
- Religious obligation and significance
- Eligibility requirements
- Nisab thresholds
- Zakat principles and rules

This content helps users understand the context and requirements before performing calculations.

2. Zakat Calculation Engine

The application provides calculators for multiple asset classes commonly considered in Zakat calculations:

- Cash holdings
- Gold assets
- Brokerage accounts / stocks
- Traditional 401(k)
- Traditional IRA
- Roth 401(k)
- Roth IRA

Each calculator handles the specific rules applicable to that asset category.

Additionally, the application includes a Quick Combined Calculator that aggregates different asset categories to estimate a user's total Zakat obligation.

## Calculation Logic

All Zakat calculations are implemented in C# domain logic within the client application. The logic includes:

- Nisab threshold checks
- Asset valuation input handling
- Zakat rate calculation (typically 2.5%)
- Aggregation across multiple asset categories

The design allows calculation logic to remain deterministic, testable, and reusable.

## Performance Considerations

Since the application runs entirely in the browser:

- No sensitive financial data is transmitted to a backend service
- Calculations execute locally on the user's device
- Initial load downloads the WebAssembly runtime and application assemblies
- Subsequent interactions are instantaneous

This approach provides privacy, responsiveness, and scalability.

## Extensibility

The system is designed to allow future enhancements, including:

- Additional asset calculators
- Updated Nisab values
- Localization and multilingual support
- Enhanced financial asset models
- Optional backend APIs for dynamic data (e.g., gold prices)