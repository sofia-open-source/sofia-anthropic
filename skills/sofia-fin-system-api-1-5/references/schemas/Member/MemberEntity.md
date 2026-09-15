# MemberEntity

**Type:** object

## Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `id` | string | Yes | Id da associação membro/organização. |
| `user` | string | Yes | Id do usuário membro. |
| `email` | string (email) | Yes | Email do membro. |
| `role` | enum: org:admin, org:member | Yes | Papel do membro na organização. |
| `firstName` | string | No | Primeiro nome do membro. |
| `lastName` | string | No | Sobrenome do membro. |
| `imageUrl` | string | No | Url da foto do membro. |
| `createdAt` |  | Yes | Data de criação do membro. |
| `updatedAt` |  | Yes | Data de atualização do membro. |

