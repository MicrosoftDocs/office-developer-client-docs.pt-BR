---
title: Propriedade CommandType (ADO)
TOCTitle: CommandType Property (ADO)
ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15)
ms:contentKeyID: 48547663
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231125
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 3cff3c3540208b142fc13cd79eb83bd218814873
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25465432"
---
# <a name="commandtype-property-ado"></a>Propriedade CommandType (ADO)


**Aplica-se a**: Access 2013 | Office 2013

Indica o tipo de um objeto [Command](command-object-ado.md).

## <a name="settings-and-return-values"></a>Configurações e valores de retorno

Define ou retorna um ou mais valores [CommandTypeEnum](commandtypeenum.md).


> [!NOTE]
> <P>[!OBSERVAçãO] Não use valores <STRONG>CommandTypeEnum</STRONG> de <STRONG>adCmdFile</STRONG> ou <STRONG>adCmdTableDirect</STRONG> com <STRONG>CommandType</STRONG>. Esses valores podem ser usados somente como opções com os métodos <A href="open-method-ado-recordset.md">Open</A> e <A href="requery-method-ado.md">Requery</A> de um <A href="recordset-object-ado.md">Recordset</A>.</P>



## <a name="remarks"></a>Comentários

Use a propriedade **CommandType** para otimizar a avaliação da propriedade [CommandText](commandtext-property-ado.md).

Se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), talvez você tenha uma diminuição do desempenho, pois o ADO deve fazer chamadas para o provedor para determinar se a propriedade **CommandText** é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).

