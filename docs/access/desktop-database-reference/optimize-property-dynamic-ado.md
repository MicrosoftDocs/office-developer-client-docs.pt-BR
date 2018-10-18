---
title: Propriedade Optimize -- Dinâmica (ADO)
TOCTitle: Optimize Property--Dynamic (ADO)
ms:assetid: 2253b052-2d8a-f6f0-f8b8-f56e79d243de
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249001(v=office.15)
ms:contentKeyID: 48543705
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7276e642e15137bdcfcb939330a3642d96e9a5a2
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605174"
---
# <a name="optimize-property--dynamic-ado"></a>Propriedade Optimize -- Dinâmica (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Especifica se um índice deve ser criado em um campo

<<<<<<< Cabeça
## <a name="settings-and-return-values"></a>Configurações e valor de retorno
=======
## <a name="settings-and-return-values"></a>Configurações e valores de retorno
>>>>>>> mestre

Define ou retorna um valor **Boolean** que indica se um índice deve ser criado.

## <a name="remarks"></a>Comentários

Um índice pode melhorar o desempenho das operações que localizam ou classificam valores em um [Recordset](recordset-object-ado.md). O índice é interno para o ADO  você não pode acessar explicitamente ou usá-lo em seu aplicativo.

Para criar um índice em um campo, defina a propriedade **Optimize** como **True**. Para excluir o índice, defina essa propriedade como **False**.

**Optimize** é uma propriedade dinâmica acrescentada à coleção [Properties](field-object-ado.md) do objeto [Field](properties-collection-ado.md) quando a propriedade [CursorLocation](cursorlocation-property-ado.md) estiver definida como **adUseClient**.

**Usage**

```vb
    Dim rs As New Recordset
    Dim fld As Field
    rs.CursorLocation = adUseClient      'Enable index creation
    rs.Fields.Append "Field1", adChar, 35, adFldIsNullable
    rs.Open
    Set fld = rs.Fields(0)
    fld.Properties("Optimize") = True    'Create an index
    fld.Properties("Optimize") = False   'Delete an index
```
