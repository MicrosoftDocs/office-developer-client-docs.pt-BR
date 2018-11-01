---
title: Objetos e Interfaces do ADO
TOCTitle: ADO Objects and Interfaces
ms:assetid: bebf4a80-8b6e-c43c-4138-897055cc60d3
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249927(v=office.15)
ms:contentKeyID: 48547471
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: efab7ce2980393282ee1f96295206e712fcbd15f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882179"
---
# <a name="ado-objects-and-interfaces"></a>Objetos e Interfaces do ADO


**Aplica-se a**: Access 2013, o Office 2013

As relações entre esses objetos são representadas no Modelo de objeto do ADOX.

Cada objeto pode estar contido em sua coleção correspondente. Por exemplo, um objeto [Error](error-object-ado.md) pode estar contido em uma coleção [Errors](errors-collection-ado.md). Para obter mais informações, consulte [Coleções do ADO](ado-collections.md) ou um tópico de coleção específico.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><a href="adorecordconstruction-interface-ado.md">ADORecordConstruction</a></p></td>
<td><p>Constrói um objeto <strong>Record</strong> do ADO a partir de um objeto <strong>Row</strong> do OLE DB em um aplicativo C/C++.</p></td>
</tr>
<tr class="even">
<td><p><a href="adorecordsetconstruction-interface-ado.md">ADORecordsetConstruction</a></p></td>
<td><p>Constrói um objeto <strong>Recordset</strong> do ADO a partir de um objeto <strong>Rowset</strong> do OLE DB em um aplicativo C/C++.</p></td>
</tr>
<tr class="odd">
<td><p><a href="error-object-ado.md">Erro</a></p></td>
<td><p>Contém os detalhes sobre os erros de acesso aos dados que pertencem à uma única operação que envolve o provedor.</p></td>
</tr>
<tr class="even">
<td><p><a href="field-object-ado.md">Field</a></p></td>
<td><p>Representa uma coluna de dados com um tipo de dados comuns.</p></td>
</tr>
<tr class="odd">
<td><p><a href="parameter-object-ado.md">Parâmetro</a></p></td>
<td><p>Representa um parâmetro ou argumento associado ao objeto <strong>Command</strong> com base em uma consulta parametrizada ou em um procedimento armazenado.</p></td>
</tr>
<tr class="even">
<td><p><a href="property-object-ado.md">Propriedade</a></p></td>
<td><p>Representa uma característica dinâmica de um objeto ADO definido pelo provedor.</p></td>
</tr>
<tr class="odd">
<td><p><a href="record-object-ado.md">Objeto Record</a></p></td>
<td><p>Representa uma linha de um <strong>Recordset</strong>, ou um diretório ou arquivo em um sistema de arquivos.</p></td>
</tr>
<tr class="even">
<td><p><a href="recordset-object-ado.md">Recordset</a></p></td>
<td><p>Representa o conjunto completo de registros de uma tabela base ou os resultados de um comando executado. Sempre que for adequado, o objeto <strong>Recordset</strong> fará referência somente a um único registro do conjunto como o registro atual.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stream-object-ado.md">Stream</a></p></td>
<td><p>Representa um fluxo de dados binário.</p></td>
</tr>
</tbody>
</table>

