---
<<<<<<< Título cabeça: propriedade MaxRecords (ADO) TOCTitle: propriedade MaxRecords (ADO) === título: a propriedade MaxRecords (ADO) TOCTitle: a propriedade MaxRecords (ADO)
>>>>>>> ms:assetid de mestre: 424b2d41-073a-3fbe-30aa-99fac94f9a81 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249195(v=office.15) ms:contentKeyID: ms.date 48544475: 18/09/2015 mtps_version: v=office.15
---

<<<<<<< Cabeça
# <a name="maxrecords-property-ado"></a>Propriedade MaxRecords (ADO)
=======
# <a name="maxrecords-property-ado"></a>Propriedade MaxRecords (ADO)
>>>>>>> mestre


**Aplica-se a**: Access 2013 | Office 2013

Indica o número máximo de registros a serem retornados a um [Recordset](recordset-object-ado.md) a partir de uma consulta.

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Long** que indica o número máximo de registros a serem retornados. O padrão é zero (sem limite).

## <a name="remarks"></a>Comentários

Use a propriedade **MaxRecords** para limitar o número de registros que o provedor retorna da fonte de dados. A definição padrão dessa propriedade é zero, o que significa que o provedor retorna todos os registros solicitados.

A propriedade **MaxRecords** será leitura/gravação quando o **Recordset** estiver fechado e somente leitura quando estiver aberto.

