---
title: Propriedade Index.Required (DAO)
TOCTitle: Required Property
ms:assetid: ec8fafc4-8155-c48e-b3c8-2d9be425175a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836310(v=office.15)
ms:contentKeyID: 48548518
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052963
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 0797ed5f930d4475d03f492109c977f8494591ce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464482"
---
# <a name="indexrequired-property-dao"></a>Propriedade Index.Required (DAO)


**Aplica-se a**: Access 2013 | Office 2013

Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.

## <a name="syntax"></a>Sintaxe

*expressão* . Necessário

*expressão* Uma variável que representa um objeto **Index** .

## <a name="remarks"></a>Comentários


> [!NOTE]
> <P>[!OBSERVAçãO] Quando definir essa propriedade para um objeto <STRONG>Index</STRONG> ou um objeto <STRONG>Field</STRONG>, defina-a para o objeto <STRONG>Field</STRONG>. A validade da definição da propriedade para um objeto <STRONG>Field</STRONG> é verificada antes da validade do objeto <STRONG>Index</STRONG>.</P>



A disponibilidade da propriedade **Required** depende do objeto que contém a coleção [Fields](fields-collection-dao.md), como exibido na tabela a seguir.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Se a coleção Fields pertencer a um</p></th>
<th><p>Então Required será</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>							Objeto <strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>							Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>							Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>

