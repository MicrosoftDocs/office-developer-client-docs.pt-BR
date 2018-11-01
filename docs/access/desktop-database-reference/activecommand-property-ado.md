---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 473a0b99310d2eb5e050ed50f1e331cb65174ae8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869558"
---
# <a name="activecommand-property-ado"></a>Propriedade ActiveCommand (ADO)

**Aplica-se a**: Access 2013, o Office 2013

Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.

## <a name="return-value"></a>Valor de retorno

Retorna um **Variant** contendo um objeto **Command**. O padrão é uma referência nula ao objeto.

## <a name="remarks"></a>Comentários

A propriedade **ActiveCommand** é somente leitura.

Se um objeto **Command** não foi usado para criar o **Recordset**atual, uma referência de objeto **nula** será retornada.

Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.

