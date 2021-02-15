---
title: Propriedade ActiveCommand (ADO)
TOCTitle: ActiveCommand property (ADO)
ms:assetid: 41c19008-cbf7-ade9-b4ab-e908a16784ac
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249190(v=office.15)
ms:contentKeyID: 48544459
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 18fa38176f7174f27b46604c6182dfbdaa422f06
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281926"
---
# <a name="activecommand-property-ado"></a>Propriedade ActiveCommand (ADO)

**Aplica-se ao:** Access 2013, Office 2013

Indica o objeto [Command](command-object-ado.md) que criou o objeto [Recordset](recordset-object-ado.md) associado.

## <a name="return-value"></a>Valor de retorno

Retorna um **Variant** contendo um objeto **Command**. O padrão é uma referência nula ao objeto.

## <a name="remarks"></a>Comentários

A propriedade **ActiveCommand** é somente leitura.

Se um **objeto Command** não tiver sido usado para criar o **Recordset atual,** uma referência de objeto **Null** será retornada.

Use essa propriedade para encontrar o objeto **Command** associado quando receber apenas o objeto **Recordset** resultante.

