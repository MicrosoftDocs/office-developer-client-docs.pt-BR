---
title: Suporte do provedor para ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301096"
---
# <a name="provider-support-for-adox"></a>Suporte do provedor para ADOX


**Aplica-se ao:** Access 2013, Office 2013

Determinados recursos do ADOX não têm suporte, dependendo do provedor de dados OLE DB. O ADOX tem suporte completo do [OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Os recursos que não têm o suporte do [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), do [Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md) ou do [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) são listados a seguir. O ADOX não tem o suporte de nenhum outro provedor Microsoft OLE DB.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Microsoft OLE DB Provider for SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto ou coleção</p></th>
<th><p>Restrições de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>Não há suporte para o método <strong>Create</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Tables</strong></p></td>
<td><p>As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Views</strong></p></td>
<td><p>Não há suporte para <strong>Views</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Procedures</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>Não há suporte para a propriedade <strong>Command</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Keys</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Users</strong></p></td>
<td><p>Não há suporte para <strong>Users</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Groups</strong></p></td>
<td><p>Não há suporte para <strong>Groups</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB Provider for ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto ou coleção</p></th>
<th><p>Restrições de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>Não há suporte para o método <strong>Create</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Tables</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>. As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Procedures</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>Não há suporte para a propriedade <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Indexes</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Keys</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Users</strong></p></td>
<td><p>Não há suporte para <strong>Users</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Groups</strong></p></td>
<td><p>Não há suporte para <strong>Groups</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB Provider for Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Objeto ou coleção</p></th>
<th><p>Restrições de uso</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Objeto <strong>Catalog</strong></p></td>
<td><p>Não há suporte para o método <strong>Create</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Tables</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>. As propriedades são leitura/gravação antes da criação do objeto, e são somente leitura quando um objeto existente é referenciado.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Views</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>View</strong></p></td>
<td><p>Não há suporte para a propriedade <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Objeto <strong>Procedures</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Objeto <strong>Procedure</strong></p></td>
<td><p>Não há suporte para a propriedade <strong>Command</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Indexes</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Keys</strong></p></td>
<td><p>Não há suporte para os métodos <strong>Append</strong> e <strong>Delete</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Coleção <strong>Users</strong></p></td>
<td><p>Não há suporte para <strong>Users</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Coleção <strong>Groups</strong></p></td>
<td><p>Não há suporte para <strong>Groups</strong>.</p></td>
</tr>
</tbody>
</table>

