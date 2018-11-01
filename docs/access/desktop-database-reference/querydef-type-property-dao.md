---
title: Propriedade QueryDef.Type (DAO)
TOCTitle: Type Property
ms:assetid: 03db891d-b958-7cf9-56c1-524d9ff2b9b5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844814(v=office.15)
ms:contentKeyID: 48542993
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c290fa743ba138a761ab19b538b2f2d292e65736
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878329"
---
# <a name="querydeftype-property-dao"></a>Propriedade QueryDef.Type (DAO)


**Aplica-se a**: Access 2013, o Office 2013

Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. **Integer** somente leitura.

## <a name="syntax"></a>Sintaxe

*expressão* . Tipo

*expressão* Uma variável que representa um objeto **QueryDef** .

## <a name="remarks"></a>Comentários

Para um objeto **QueryDef**, as configurações e os valores de retorno possíveis são mostrados na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante</p></th>
<th><p>Tipo de consulta</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbQAction</strong></p></td>
<td><p>Ação</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQAppend</strong></p></td>
<td><p>Acréscimo</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQCompound</strong></p></td>
<td><p>Composto</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQCrosstab</strong></p></td>
<td><p>Tabela de referência cruzada</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQDDL</strong></p></td>
<td><p>Definição de dados</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQDelete</strong></p></td>
<td><p>Delete</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQMakeTable</strong></p></td>
<td><p>Criar tabela</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQProcedure</strong></p></td>
<td><p>Procedimento (somente em espaços de trabalho ODBCDirect)</p>

> [!NOTE]
> <P>[!OBSERVAçãO] O Microsoft Access 2013 não oferece suporte para espaços de trabalho ODBCDirect. Use ADO para acessar fontes de dados externas sem usar o mecanismo de banco de dados do Microsoft Access.</P>


<p></p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSelect</strong></p></td>
<td><p>Selecionar</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSetOperation</strong></p></td>
<td><p>União</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQSPTBulk</strong></p></td>
<td><p>Usado com <strong>dbQSQLPassThrough</strong> para especificar um consulta que não retorna registros (somente em espaços de trabalho do Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong>dbQSQLPassThrough</strong></p></td>
<td><p>Passagem (somente em espaços de trabalho do Microsoft Access)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbQUpdate</strong></p></td>
<td><p>Atualizar</p></td>
</tr>
</tbody>
</table>


Quando você acrescentar um novo objeto **[Field](field-object-dao.md)**, **[Parameter](parameter-object-dao.md)** ou **[Property](property-object-dao.md)** à coleção de um objeto **[Index](index-object-dao.md)**, **QueryDef**, **[Recordset](recordset-object-dao.md)** ou **[TableDef](tabledef-object-dao.md)**, ocorrerá um erro, caso o banco de dados base não ofereça suporte ao tipo de dados especificado para o novo objeto.

