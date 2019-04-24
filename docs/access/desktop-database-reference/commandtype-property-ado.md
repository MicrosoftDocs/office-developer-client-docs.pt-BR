---
title: Propriedade CommandType (ADO)
TOCTitle: CommandType property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c978a6a227266fa43c1102fc109be2b81262de8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296119"
---
# <a name="commandtype-property-ado"></a>Propriedade CommandType (ADO)


**Aplica-se ao:** Access 2013, Office 2013

Indica o tipo de um objeto [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um ou mais valores [CommandTypeEnum](commandtypeenum.md).

> [!NOTE]
> [!OBSERVAçãO] Não use valores **CommandTypeEnum** de **adCmdFile** ou **adCmdTableDirect** com **CommandType**. Esses valores podem ser usados somente como opções com os métodos [Open](open-method-ado-recordset.md) e [Requery](requery-method-ado.md) de um [Recordset](recordset-object-ado.md).


## <a name="remarks"></a>Comentários

Use a propriedade **CommandType** para otimizar a avaliação da propriedade [CommandText](commandtext-property-ado.md).

Se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), talvez você tenha uma diminuição do desempenho, pois o ADO deve fazer chamadas para o provedor para determinar se a propriedade **CommandText** é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).

