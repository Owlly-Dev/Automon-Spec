# Backend Specifications
## Brief Specs
* should be able to gracefully handle the test suite executions.
* must have an eventful execution.
* must support two browsers Mozilla and Chrome(for now).
* should support subscription tiers for customers.
* Reporting of test suite execution on every run based on customer configuration.
* should support customer level roles for org use cases.
* code written should be maintanable.(very important bigulu!)
* must support scheduling of suite executions.

## Data Structure
 ┌────────────┐  has  ┌──────────┐
 │    Users   ├───────►   Roles  │
 └─────┬──────┘  one  └──────────┘
       │has many
       │
┌──────▼──────┐ has ┌─────────────┐
│ Test Suites ├─────► Credentials │
└──────┬──┬───┘many └─────────────┘
    has│  │has
   many│  │many
       │  └─────────────────┐
┌──────▼──────┐       ┌─────▼────┐
│   Features  │       │  Reports │
└───────┬─┬───┘       └──────────┘
     has│ │  ┌────────────┐
    many│ └──► step Defs  │
        │    └────────────┘
┌───────▼──────┐
│  Test Cases  │
└──────────────┘