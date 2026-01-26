# PRD: {{APP_NAME}} MVP

## Introduction

{{APP_DESCRIPTION}}

**Target Users:** {{TARGET_USERS}}

**Core Value:** {{VALUE_PROPOSITION}}

---

## Goals

- {{GOAL_1}}
- {{GOAL_2}}
- {{GOAL_3}}

---

## User Stories

### US-001: {{USER_STORY_TITLE}}
**Description:** As a {{USER_TYPE}}, I want to {{ACTION}} so that {{BENEFIT}}.

**Acceptance Criteria:**
- [ ] {{CRITERION_1}}
- [ ] {{CRITERION_2}}
- [ ] {{CRITERION_3}}
- [ ] Typecheck passes
- [ ] Verify in browser

### US-002: {{USER_STORY_TITLE}}
**Description:** As a {{USER_TYPE}}, I want to {{ACTION}} so that {{BENEFIT}}.

**Acceptance Criteria:**
- [ ] {{CRITERION_1}}
- [ ] {{CRITERION_2}}
- [ ] Typecheck passes
- [ ] Verify in browser

### US-003: {{USER_STORY_TITLE}}
**Description:** As a {{USER_TYPE}}, I want to {{ACTION}} so that {{BENEFIT}}.

**Acceptance Criteria:**
- [ ] {{CRITERION_1}}
- [ ] {{CRITERION_2}}
- [ ] Typecheck passes
- [ ] Verify in browser

<!--
Add more user stories as needed. Each should have:
- Clear description with user type, action, benefit
- Specific, testable acceptance criteria
- Typecheck and browser verification criteria
-->

---

## Functional Requirements

### {{DOMAIN_1}}
- FR-1: {{REQUIREMENT}}
- FR-2: {{REQUIREMENT}}

### {{DOMAIN_2}}
- FR-3: {{REQUIREMENT}}
- FR-4: {{REQUIREMENT}}

### {{DOMAIN_3}}
- FR-5: {{REQUIREMENT}}
- FR-6: {{REQUIREMENT}}

---

## Non-Goals (Out of Scope for MVP)

- **{{FEATURE}}:** {{REASON_WHY_OUT_OF_SCOPE}}
- **{{FEATURE}}:** {{REASON_WHY_OUT_OF_SCOPE}}
- **{{FEATURE}}:** {{REASON_WHY_OUT_OF_SCOPE}}

---

## Technical Considerations

### Stack
- **Framework:** {{FRAMEWORK}}
- **Database:** {{DATABASE}}
- **Auth:** {{AUTH_SOLUTION}}
- **UI:** {{UI_LIBRARY}}
- **Deployment:** {{DEPLOYMENT_PLATFORM}}

### Data Schema
```typescript
{{DATA_SCHEMA}}
```
<!--
Example:
interface User {
  id: string;
  email: string;
  name: string;
  createdAt: Date;
}

interface Project {
  id: string;
  userId: string;
  name: string;
  status: "draft" | "active" | "complete";
}
-->

---

## Success Metrics

- {{METRIC_1}}
- {{METRIC_2}}
- {{METRIC_3}}

---

## Open Questions

1. {{QUESTION_1}}
2. {{QUESTION_2}}

<!--
Document decisions as they're made:

## Resolved Questions

1. **{{QUESTION}}:** {{DECISION_AND_REASONING}}
-->
