---
title: Membros de parâmetro (DAO)
TOCTitle: Parameter Members
ms:assetid: 38e19de8-5318-6077-13b1-10653069aaeb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192517(v=office.15)
ms:contentKeyID: 48544228
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25eae70d88307331c44983c4e7cbbcce3fe9d309
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288109"
---
# <a name="parameter-members-dao"></a>Membros de parâmetro (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Um objeto Parameter representa um valor fornecido para uma consulta. O parâmetro está associado ao objeto QueryDef criado a partir de uma consulta parâmetro.

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
<td><p><strong><a href="parameter-direction-property-dao.md">Direction</a></strong></p></td>
<td><p><strong>Observação</strong>: os espaços de trabalho ODBCDirect não têm suporte no Microsoft Access 2013. Use o ADO se você quiser acessar fontes de dado externas sem usar o mecanismo de banco de dados do Microsoft Access.</p>
<p>Define ou retorna um valor que indica se um objeto <strong><a href="parameter-object-dao.md">Parameter</a></strong> representa um parâmetro de entrada, um parâmetro de saída, ambos ou o valor de retorno do procedimento (apenas espaços de trabalho do ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-name-property-dao.md">Nome</a></strong></p></td>
<td><p>Retorna o nome do objeto especificado. Somente leitura <strong>cadeia de caracteres</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-properties-property-dao.md">Propriedades</a></strong></p></td>
<td><p>Retorna a coleção <strong><a href="properties-collection-dao.md">Properties</a></strong> do objeto especificado. Somente leitura.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="parameter-type-property-dao.md">Tipo</a></strong></p></td>
<td><p>Define ou retorna um valor que indica o tipo operacional ou o tipo de dados de um objeto. <strong>Integer</strong> de leitura/gravação.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="parameter-value-property-dao.md">Valor</a></strong></p></td>
<td><p>Define ou retorna o valor de um objeto. <strong>Variant</strong> de leitura/gravação.</p></td>
</tr>
</tbody>
</table>

