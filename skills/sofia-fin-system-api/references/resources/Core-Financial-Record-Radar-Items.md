# Core - Financial Record Radar Items

Represents the intent to create(one or many)/update financial records on the system based on a WhatsApp message or email.

## Operations

| Method | Path | Summary | Details |
|--------|------|---------|----------|
| GET | `/core/financial-records/radar/items` | Busca todos os registros do radar. | [View](../operations/coreFindAllFinancialRecordRadarItems.md) |
| POST | `/core/financial-records/radar/items/{radarItemId}/links` | Vincula registros financeiros a um registro de radar | [View](../operations/coreLinkFinancialRecordsToFinancialRecordRadarItem.md) |
| GET | `/core/financial-records/radar/items/{radarItemId}` | Busca um registro de radar pelo identificador. | [View](../operations/coreFindByIdFinancialRecordRadarItem.md) |
| PATCH | `/core/financial-records/radar/items/{radarItemId}` | Atualiza parcialmente um registro de radar | [View](../operations/corePartialUpdateFinancialRecordRadarItem.md) |
| GET | `/core/financial-records/radar/items/{radarItemId}/tags` | Obtém as tags para um registro de radar. | [View](../operations/coreGetTagsForFinancialRecordRadarItem.md) |
| GET | `/core/financial-records/radar/items/{radarItemId}/preview-bulk-create-file` | Obtém o preview de um arquivo .csv para criação em lote. | [View](../operations/corePreviewBulkCreateFile.md) |
| POST | `/core/financial-records/radar/items/{radarItemId}/unlink` | Desvincula registros financeiros de um registro de radar | [View](../operations/coreUnlinkFinancialRecordsFromFinancialRecordRadarItem.md) |
