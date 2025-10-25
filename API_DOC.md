
base URL: http://localhost:3000

# Task Management API

A backend API built with Node.js, Express, and Prisma for task management.

## 🔐 Authentication Routes

**Base:** `/api/auth`

| Method | Endpoint | 
|--------|-----------|
| POST | `/register` | 
| POST | `/login` | 

---

# Task Routes #

1. GET /tasks

# Parameters#
| Code    | Description                      |
| ------- | -------------------------------- |
| **200** | Successfully retrieved all tasks |
| **500** | Server error                     |


2. GET /tasks/:id

# Parameters#

| Name | Type     | Required | Description                       |
| ---- | -------- | -------- | --------------------------------- |
| `id` | `string` | ✅        | The unique identifier of the task |

 # Status codes #

| Code    | Description            |
| ------- | ---------------------- |
| **200** | Successfully retrieved |
| **404** | Task not found         |
| **500** | Server error           |



3. POST /tasks
# Parameters#

| Name          | Type     | Required | Description                |
| ------------- | -------- | -------- | -------------------------- |
| `title`       | `string` | ✅        | The title of the task      |
| `description` | `string` | ❌        | Details about the task     |
| `dueDate`     | `string` | ❌        | Task due date (ISO format) |

# Status codes #

| Code    | Description                    |
| ------- | ------------------------------ |
| **201** | Task created successfully      |
| **400** | Bad request (validation error) |


1. PUT /tasks/:id
# Parameters#

| Name | Type     | Required | Description                  |
| ---- | -------- | -------- | ---------------------------- |
| `id` | `string` | ✅        | The ID of the task to update |

# Status codes #
| Code    | Description          |
| ------- | -------------------- |
| **200** | Successfully updated |
| **404** | Task not found       |
| **400** | Invalid input data   |

5. DELETE /tasks/:id

# Parameters#
| Name | Type     | Required | Description                  |
| ---- | -------- | -------- | ---------------------------- |
| `id` | `string` | ✅        | The ID of the task to delete |


# Status codes #  

| Code    | Description          |
| ------- | -------------------- |
| **200** | Successfully deleted |
| **404** | Task not found       |
| **500** | Server error         |


6. GET /tasks/:taskId/subtasks

# Parameters#
| Name     | Type     | Required | Description               |
| -------- | -------- | -------- | ------------------------- |
| `taskId` | `string` | ✅        | The ID of the parent task |


# Status codes # 

| Code    | Description                         |
| ------- | ----------------------------------- |
| **200** | Successfully retrieved all subtasks |
| **404** | Task not found or access denied     |
| **500** | Server error                        |

7. GET /subtasks/:id
# Parameters#

| Name | Type     | Required | Description                          |
| ---- | -------- | -------- | ------------------------------------ |
| `id` | `string` | ✅        | The unique identifier of the subtask |


# status codes #  

| Code    | Description                        |
| ------- | ---------------------------------- |
| **200** | Successfully retrieved             |
| **404** | Subtask not found or access denied |
| **500** | Server error                       |

8. POST /tasks/:taskId/subtasks

# Parameters#

| Name     | Type     | Required | Description               |
| -------- | -------- | -------- | ------------------------- |
# Parameters #

| `taskId` | `string` | ✅        | The ID of the parent task |

# Body Parameters # 

| Name          | Type     | Required | Description                              |
| ------------- | -------- | -------- | ---------------------------------------- |
| `title`       | `string` | ✅        | The title of the subtask                 |
| `description` | `string` | ❌        | Description of the subtask               |
| `status`      | `string` | ❌        | Subtask status (e.g., "pending", "done") |


# Status codes #  

| Code    | Description                     |
| ------- | ------------------------------- |
| **201** | Subtask created successfully    |
| **401** | Task not found or access denied |
| **400** | Bad request                     |


9. PUT /subtasks/:id

# Parameters # 
| Name | Type     | Required | Description                     |
| ---- | -------- | -------- | ------------------------------- |
| `id` | `string` | ✅        | The ID of the subtask to update |

# Status codes # 

| Code    | Description                        |
| ------- | ---------------------------------- |
| **200** | Successfully updated               |
| **404** | Subtask not found or access denied |
| **400** | Invalid input data                 |

10.  DELETE /subtasks/:id

 # Parameters # 

| Name | Type     | Required | Description                     |
| ---- | -------- | -------- | ------------------------------- |
| `id` | `string` | ✅        | The ID of the subtask to delete |


 # Status codes # 

| Code    | Description                        |
| ------- | ---------------------------------- |
| **200** | Successfully deleted               |
| **404** | Subtask not found or access denied |
| **500** | Server error                       |






---



