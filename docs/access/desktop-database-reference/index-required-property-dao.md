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
localization_priority: Normal
ms.openlocfilehash: a2660a4cb422d91cf46b98a8d3870d2ab2db73fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291696"
---
# <a name="indexrequired-property-dao"></a>Propriedade Index.Required (DAO)

**Aplica-se ao:** Access 2013, Office 2013

Define ou retorna um valor que indica se um objeto **[Field](field-object-dao.md)** requer um valor não Null.

## <a name="syntax"></a>Sintaxe

*expressão* . Obrigatório

*expressão* Uma variável que representa um **objeto Index** .

## <a name="remarks"></a>Comentários

> [!NOTE]
> [!OBSERVAçãO] Quando definir essa propriedade para um objeto **Index** ou um objeto **Field**, defina-a para o objeto **Field**. A validade da definição da propriedade para um objeto **Field** é verificada antes da validade do objeto **Index**.

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
<td><p>
						Objeto <strong>Index</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>QueryDef</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>Recordset</strong></p></td>
<td><p>Somente leitura</p></td>
</tr>
<tr class="even">
<td><p>
						Objeto <strong>Relation</strong></p></td>
<td><p>Sem suporte</p></td>
</tr>
<tr class="odd">
<td><p>
						Objeto <strong>TableDef</strong></p></td>
<td><p>Leitura/gravação</p></td>
</tr>
</tbody>
</table>

