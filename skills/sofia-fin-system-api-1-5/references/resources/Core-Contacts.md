# Core - Contacts

People and companies (customers, suppliers, employees) linked to financial records. Full CRUD plus paginated list, find-by-id, and org-scoped lookups. Reference endpoints expose contact types and origins. Includes lookup of the special not-identified contact used when no counterparty is known.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/contacts` | Busca todos os contatos. | [View](../operations/coreFindAllContacts.md) |
| POST | `/core/contacts` | Cria um novo contato. | [View](../operations/coreCreateContact.md) |
| GET | `/core/contacts/{id}` | Busca um contato pelo identificador. | [View](../operations/coreFindByIdContact.md) |
| DELETE | `/core/contacts/{id}` | Remove um contato. | [View](../operations/coreRemoveContact.md) |
| PATCH | `/core/contacts/{id}` | Atualiza parcialmente um contato. | [View](../operations/corePartialUpdateContact.md) |
| GET | `/core/contacts/types` | Busca todos os tipos de contato. | [View](../operations/coreFindAllContactTypes.md) |
| GET | `/core/contacts/origins` | Busca todas as origens de contato. | [View](../operations/coreFindAllContactOrigins.md) |
| GET | `/core/organizations/{organizationId}/contacts/not-identified` | Busca o contato não identificado. | [View](../operations/coreFindNotIdentifiedContact.md) |
