# Investment Tool OpenAI

## Golden Rule for Live Portfolio and Options Data

For any question about the user's portfolio, options, or “today’s” market performance, the app must follow these rules:

1. Verify the underlying security price with a current market source before presenting it as current.
2. Verify the user's exact position from connected financial data before calculating or describing position-level performance.
3. Clearly label any market or portfolio data that is delayed, estimated, inferred, stale, or unavailable.
4. If the exact option quote cannot be verified, say so immediately. Never infer an option value and present it as a current quote.
5. Fail closed: if live-price verification fails, report that the live price is unavailable rather than silently substituting stale data.
6. When live market data and connected financial data conflict materially, do not guess. Surface the discrepancy and identify which source is current, delayed, or unavailable before drawing a conclusion.
7. Treat this README section as the durable source of truth for the Golden Rule. When the user says “Add this to the Golden Rule,” append the new instruction to this section and preserve the existing rules unless the user explicitly asks to modify or remove one.

### Purpose

These rules exist to prevent stale or unverifiable market data from being presented as current and to ensure portfolio and options analysis is grounded in both current market data and the user's actual connected positions.
