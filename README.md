# @sudobility/shaperouter_types

Shared TypeScript type definitions for the ShapeRouter LLM structured output platform.

## Installation

```bash
bun add @sudobility/shaperouter_types
```

## Usage

```typescript
import type {
  User, Project, Endpoint, LlmProvider,
  AiExecutionRequest, AiExecutionResponse,
} from '@sudobility/shaperouter_types';

import { successResponse, errorResponse } from '@sudobility/shaperouter_types';
```

## Types

- **Enums**: `LlmProvider` (openai, gemini, anthropic, lm_studio), `HttpMethod`
- **Entities**: `User`, `LlmApiKey` / `LlmApiKeySafe`, `Project`, `Endpoint`, `UsageAnalytics`, `UserSettings`
- **Requests**: Create/Update types for users, keys, projects, endpoints, plus `AiExecutionRequest`
- **Responses**: `AiExecutionResponse`, `AiPromptResponse`, `AnalyticsResponse`, `HealthCheckData`
- **Query Params**: `ProjectQueryParams`, `EndpointQueryParams`, `UsageAnalyticsQueryParams`
- **Utilities**: `JsonSchema`, `ApiResponse<T>`, `PaginatedResponse<T>` (re-exported from `@sudobility/types`)
- **Helpers**: `successResponse()`, `errorResponse()` (runtime functions)

## Development

```bash
bun run build        # Build ESM + CJS
bun run test         # Run Vitest
bun run typecheck    # TypeScript check
bun run lint         # ESLint
bun run verify       # Typecheck + lint + build
```

## Related Packages

- `@sudobility/shaperouter_client` -- React hooks for ShapeRouter API
- `@sudobility/shaperouter_lib` -- Business logic with Zustand stores
- `shaperouter_api` -- Backend API server
- `shaperouter_app` -- Frontend web application

## License

BUSL-1.1
