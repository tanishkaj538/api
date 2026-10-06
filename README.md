# Switchly API

A feature flag management API built with Java and Spring Boot. Flags are organized as **Organization → Project → Flag**, and each flag can be turned on or off.

## Tech stack
- Java, Spring Boot, Maven
- REST API with validation and error handling (400, 404, 409)
- In-memory storage

## Run locally
```bash
git clone https://github.com/deepanshuguptacse2024-create/SwitchlyApiApplication.git
cd SwitchlyApiApplication
./mvnw spring-boot:run
```
Server starts on `http://localhost:8080`.

## API endpoints

| Method | Path | Description |
|---|---|---|
| POST | `/api/v1/orgs`| Create a Organizations |
| GET | `/api/v1/orgs/{orgsId}` | list a Organization |
| POST | `/api/v1/orgs/{orgsId}/projects` | create a project |
| GET | `/api/v1/projects/{projectsId}` | list a projects |
| POST | `/api/v1/projects/{projectId}/flags` | Create a flag |
| GET | `/api/v1/projects/{projectId}/flags` | List flags of a project |
| PUT| `[apna path]` | Turn a flag on/off |

### Create a flag
Request body:
```json
{
  "key": "new-dashboard",
  "name": "New dashboard",
  "description": "Optional note about the flag"
}
```
- `key`: required, only lowercase letters, numbers and hyphens
- `name`: required
- `description`: optional

Response: `201 Created`

## Error responses
| Status | When |
|---|---|
| 400 | Invalid input (blank name, bad key format) |
| 404 | Project or flag not found |
| 409 | Flag key already exists in the project |

## Screenshots


## create a organization:
<img width="743" height="620" alt="Screenshot 2026-10-06 125158" src="https://github.com/user-attachments/assets/84396d91-ff34-4269-ae9b-a39b9c12076d" />
## list a organization :
<img width="759" height="639" alt="Screenshot 2026-10-06 125247" src="https://github.com/user-attachments/assets/78e45993-6530-4f90-94b8-3d48eb94c138" />
## create a projects :
<img width="729" height="602" alt="Screenshot 2026-10-06 125455" src="https://github.com/user-attachments/assets/670d1b69-4747-405d-b072-7b9bff92c4b5" />
## list a projects :
<img width="707" height="618" alt="Screenshot 2026-10-06 125534" src="https://github.com/user-attachments/assets/8ec2e6cf-e80b-4024-825d-36358384803a" />
## Create a flag:
<img width="700" height="624" alt="Screenshot 2026-10-06 125913" src="https://github.com/user-attachments/assets/746d42ff-6daa-4aa1-8afa-cbe4d3f32e05" />
## list a access of flag :
<img width="698" height="567" alt="Screenshot 2026-10-06 125642" src="https://github.com/user-attachments/assets/33aa053a-2e6d-4afd-954d-b3a88a18ab89" />

### Turn flag on/off
<img width="708" height="586" alt="Screenshot 2026-10-06 130153" src="https://github.com/user-attachments/assets/0a6d6859-40c4-4f39-a517-28031434ab4d" />
