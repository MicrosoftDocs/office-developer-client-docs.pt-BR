---
title: Membros de TableDef (DAO)
TOCTitle: TableDef Members
ms:assetid: bc55315e-bafe-d89e-ad31-fd4c9bb6486e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822714(v=office.15)
ms:contentKeyID: 48547408
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 405bf207fc29106f9b80944d0d2bbee8907d3070
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25463887"
---
# <a name="tabledef-members-dao"></a>Membros de TableDef (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Um objeto TableDef representa a definição armazenada de uma tabela base ou de uma tabela vinculada (apenas espaços de trabalho do Microsoft Access).

## <a name="methods"></a>Métodos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="tabledef-createfield-method-dao.md">CreateField</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="field-object-dao.md">Field</a></strong> (apenas espaços de trabalho do Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-createindex-method-dao.md">CreateIndex</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="index-object-dao.md">Index</a></strong> (apenas espaços de trabalho do Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Cria um novo objeto <strong><a href="property-object-dao.md">Property</a></strong> definido pelo usuário (somente espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Cria e anexa um novo objeto <strong><a href="recordset-object-dao.md">Recordset</a></strong> à coleção <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-refreshlink-method-dao.md">RefreshLink</a></strong></p></td>
<td><p>Atualiza as informações de conexão para uma tabela vinculada (apenas espaços de trabalho do Microsoft Access).</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Propriedades

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Nome</p></th>
<th><p>Descrição</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="tabledef-attributes-property-dao.md">Atributos</a></strong></p></td>
<td><p>Define ou retorna um valor que indica uma ou várias características de um objeto <strong>TableDef</strong>. <strong>Long</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-conflicttable-property-dao.md">ConflictTable</a></strong></p></td>
<td><p>Retorna o nome de uma tabela em conflito que contém os registros do banco de dados que estavam em conflito durante a sincronização de duas réplicas (apenas espaços de trabalho do Microsoft Access). <strong>String</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Define ou retorna um valor que fornece informações sobre uma tabela vinculada. <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Retorna a hora e a data nas quais um objeto foi criado (somente em espaços de trabalho do Microsoft Access). <strong>Variant</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Fields</strong> que representa todos os objetos <strong>Field</strong> armazenados para o objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-indexes-property-dao.md">Indexes</a></strong></p></td>
<td><p>Retorna uma coleção <strong>Indexes</strong> que contém todos os objetos <strong>Index</strong> armazenados na tabela especificada. Somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Retorna a data e a hora da alteração feita mais recentemente em um objeto. <strong>Variant</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna ou define o nome do objeto especificado. <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Retorna o número total de registros de um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. <strong>Long</strong> somente leitura.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-replicafilter-property-dao.md">ReplicaFilter</a></strong></p></td>
<td><p>Define ou retorna um valor em um objeto <strong><a href="tabledef-object-dao.md">TableDef</a></strong> em uma réplica parcial que indica qual subconjunto de registros foi replicado nessa tabela a partir de uma réplica completa. (Somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o nome de uma tabela vinculada ou o nome da tabela base (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Retorna um valor que indica se você pode alterar um objeto DAO. <strong>Boolean</strong> somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="tabledef-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Define ou retorna um valor que valida os dados em um campo à medida que estes são alterados ou adicionados a uma tabela (somente em espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="tabledef-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Define ou retorna um valor que especifica o texto da mensagem exibido pelo aplicativo, caso o valor de um objeto <strong>Field</strong> não satisfaça a regra de validação especificada pela definição da propriedade <strong>ValidationRule</strong> (somente nos espaços de trabalho do Microsoft Access). <strong>String</strong> de leitura/gravação.</p></td>
</tr>
</tbody>
</table>

