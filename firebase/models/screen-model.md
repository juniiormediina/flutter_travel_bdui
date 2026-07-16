# Screen Model

## Screen

A screen is the top-level structure returned by the backend.

### Properties

| Field | Type |
|---------|---------|
| screenId | String |
| version | String |
| title | String |
| sections | Array |

---

## Section

A logical grouping of components.

### Properties

| Field | Type |
|---------|---------|
| id | String |
| components | Array |

---

## Component

Represents a renderable element.

### Properties

| Field | Type |
|---------|---------|
| id | String |
| type | String |
| props | Object |
