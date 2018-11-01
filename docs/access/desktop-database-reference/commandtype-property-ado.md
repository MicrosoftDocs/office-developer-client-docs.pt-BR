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
ms.openlocfilehash: 89264889281070b8a477c3a04b8f6f5735efdf3e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880233"
---
# <a name="commandtype-property-ado"></a><span data-ttu-id="f0630-102">Propriedade CommandType (ADO)</span><span class="sxs-lookup"><span data-stu-id="f0630-102">CommandType property (ADO)</span></span>


<span data-ttu-id="f0630-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0630-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0630-104">Indica o tipo de um objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0630-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="f0630-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="f0630-105">Settings and return values</span></span>

<span data-ttu-id="f0630-106">Define ou retorna um ou mais valores [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="f0630-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>

> [!NOTE]
> <span data-ttu-id="f0630-p101">[!OBSERVAçãO] Não use valores **CommandTypeEnum** de **adCmdFile** ou **adCmdTableDirect** com **CommandType**. Esses valores podem ser usados somente como opções com os métodos [Open](open-method-ado-recordset.md) e [Requery](requery-method-ado.md) de um [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0630-p101">Do not use the **CommandTypeEnum** values of **adCmdFile** or **adCmdTableDirect** with **CommandType**. These values can only be used as options with the [Open](open-method-ado-recordset.md) and [Requery](requery-method-ado.md) methods of a [Recordset](recordset-object-ado.md).</span></span>


## <a name="remarks"></a><span data-ttu-id="f0630-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0630-109">Remarks</span></span>

<span data-ttu-id="f0630-110">Use a propriedade **CommandType** para otimizar a avaliação da propriedade [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="f0630-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="f0630-p102">Se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), talvez você tenha uma diminuição do desempenho, pois o ADO deve fazer chamadas para o provedor para determinar se a propriedade **CommandText** é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).</span><span class="sxs-lookup"><span data-stu-id="f0630-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

