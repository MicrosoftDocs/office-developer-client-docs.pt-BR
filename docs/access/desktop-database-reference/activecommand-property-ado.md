---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand Property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f01ae4c821d8beb6c8de84c7ed671a373d7372c9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25464838"
---
# <a name="activecommand-property-ado"></a>Propriedade ActiveCommand (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.

## <a name="return-value"></a>Valor de retorno

Retorna um **Variant** contendo um objeto **Command**. O padrão é uma referência nula ao objeto.

## <a name="remarks"></a>Comentários

A propriedade **ActiveCommand** é somente leitura.

Se um objeto **Command** não tiver sido usado para criar o **Recordset** atual, então uma referência de objeto **Nula** será retornada.

Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.

