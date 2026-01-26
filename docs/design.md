# {{APP_NAME}} — Design Document

## Overview

{{DESIGN_OVERVIEW}}

---

## User Flow

```
{{USER_FLOW_DIAGRAM}}
```
<!--
Example:
Landing Page → Auth → Dashboard → Create → Edit → Preview → Publish
-->

---

## Page Layouts

### {{PAGE_1_NAME}}

```
┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  {{ASCII_WIREFRAME}}                                               │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

### {{PAGE_2_NAME}}

```
┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  {{ASCII_WIREFRAME}}                                               │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

### {{PAGE_3_NAME}}

```
┌────────────────────────────────────────────────────────────────────┐
│                                                                    │
│  {{ASCII_WIREFRAME}}                                               │
│                                                                    │
└────────────────────────────────────────────────────────────────────┘
```

<!--
Add wireframes for each page in the user flow.
Use ASCII art to show layout structure.
Include key UI elements: headers, forms, buttons, cards, etc.
-->

---

## Component Hierarchy

```
App
├── {{PROVIDER_COMPONENTS}}
└── Router
    ├── / → {{PAGE_COMPONENT}}
    │   └── {{CHILD_COMPONENTS}}
    ├── /{{ROUTE}} → {{PAGE_COMPONENT}}
    │   └── {{CHILD_COMPONENTS}}
    └── /{{ROUTE}} → {{PAGE_COMPONENT}}
        └── {{CHILD_COMPONENTS}}
```

---

## Styling

### Design Tokens

```css
/* Colors */
--color-primary: {{PRIMARY_COLOR}};
--color-success: {{SUCCESS_COLOR}};
--color-warning: {{WARNING_COLOR}};
--color-error: {{ERROR_COLOR}};

--color-bg: {{BG_COLOR}};
--color-surface: {{SURFACE_COLOR}};
--color-border: {{BORDER_COLOR}};

--color-text: {{TEXT_COLOR}};
--color-text-muted: {{MUTED_TEXT_COLOR}};
```

### Component Styling

{{STYLING_APPROACH}}
<!--
Example:
Using shadcn/ui components with Tailwind.
Prefer utility classes over custom CSS.
-->

---

## Responsive Behavior

### Desktop (> 1024px)
- {{DESKTOP_BEHAVIOR}}

### Tablet (768px - 1024px)
- {{TABLET_BEHAVIOR}}

### Mobile (< 768px)
- {{MOBILE_BEHAVIOR}}

---

## States

### Loading States
- {{LOADING_APPROACH}}

### Error States
- {{ERROR_APPROACH}}

### Empty States
- {{EMPTY_STATE_APPROACH}}

---

## Incomplete / TBD

- [ ] {{DESIGN_TODO_1}}
- [ ] {{DESIGN_TODO_2}}
- [ ] {{DESIGN_TODO_3}}

---

**Document Version:** 1.0
**Updated:** {{DATE}}
