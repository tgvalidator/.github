## TG Validator

**Real-time Telegram registration checks.**

Submit one phone number and get the Telegram registration result in the same HTTP response. Up to 100 numbers per synchronous request. Whole lists — by phone number or by username — go through the bulk task API.

[**Website**](https://tgvalidator.com) · [**API documentation**](https://tgvalidator.com/api-docs) · [**Pricing**](https://tgvalidator.com/pricing) · [**Get an API key**](https://tgvalidator.com/register)

### Official API example repositories

One repository per product, each mirroring its own product page.

| Repository | Shape | Product code | Contents |
|---|---|---|---|
| **[Telegram Registration Check](https://github.com/tgvalidator/telegram-number-checker-api)** | Realtime | `tg` | OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Telegram Bulk Activity Check](https://github.com/tgvalidator/telegram-bulk-activity-api)** | Bulk (async) | `tg_active_batch` | Input: phone · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Telegram Bulk Profile Check](https://github.com/tgvalidator/telegram-bulk-profile-api)** | Bulk (async) | `tg_profile_batch` | Input: phone · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Telegram Bulk Registration Check](https://github.com/tgvalidator/telegram-bulk-registration-api)** | Bulk (async) | `tg_batch` | Input: phone · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Telegram Bulk Username Check](https://github.com/tgvalidator/telegram-bulk-username-api)** | Bulk (async) | `tg_username_batch` | Input: username · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| **[Telegram Bulk Username Profile Check](https://github.com/tgvalidator/telegram-bulk-username-profile-api)** | Bulk (async) | `tg_username_profile_batch` | Input: username · OpenAPI contract, `product.json`, `llms.txt`, examples in 7 languages |
| [tgvalidator-resources](https://github.com/tgvalidator/tgvalidator-resources) | — | — | Technical notes, guides and announcements |

Every example repository carries a machine-readable `product.json`, an `llms.txt` summary for AI clients, an OpenAPI 3.0 contract, and runnable examples in Python, Node.js, Go, Java, C#, PHP and Shell. All request paths, response fields and limits are taken from the live product pages and the published API documentation.

### Realtime or bulk?

A **realtime** check (`POST /api/v1/check`, or `POST /api/v1/batch-check` for up to 100 identifiers) answers inside the same HTTP response — that is the shape for a signup form, a checkout step or a live lookup. A **bulk task** (`POST /api/v1/bulk-tasks`) takes a `.txt`/`.csv` file of 1,000–100,000 entries, returns a task id immediately, and produces a downloadable result file — that is the shape for list cleaning, campaign preparation and enrichment runs. The two are separate endpoints and are not interchangeable.

One bulk task carries **one product**. Phone-number tasks also carry exactly one `country`; email and username tasks have no country at all.

### One key, one balance

Every product on TG Validator uses the same API key, the same `X-API-Key` header and the same `code` / `msg` / `data` envelope, and draws from the same account balance.

### Responsible use

Results are **point-in-time signals**: they describe what a provider reported at the moment of the check. They are not identity verification, not proof of ownership, and not permission to contact anyone. Use the API only for identifiers you are authorized to process, and comply with applicable privacy laws and platform terms. Third-party trademarks belong to their respective owners; no affiliation or endorsement is implied.
