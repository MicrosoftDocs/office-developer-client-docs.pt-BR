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
# <a name="commandtype-property-ado"></a><span data-ttu-id="72616-102">Propriedade CommandType (ADO)</span><span class="sxs-lookup"><span data-stu-id="72616-102">CommandType Property (ADO)</span></span>


<span data-ttu-id="72616-103">**Aplica-se a**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="72616-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="72616-104">Indica o tipo de um objeto [Command](command-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72616-104">Indicates the type of a [Command](command-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="72616-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="72616-105">Settings and Return Values</span></span>

<span data-ttu-id="72616-106">Define ou retorna um ou mais valores [CommandTypeEnum](commandtypeenum.md).</span><span class="sxs-lookup"><span data-stu-id="72616-106">Sets or returns one or more [CommandTypeEnum](commandtypeenum.md) values.</span></span>


> [!NOTE]
> <P><span data-ttu-id="72616-p101">[!OBSERVAçãO] Não use valores <STRONG>CommandTypeEnum</STRONG> de <STRONG>adCmdFile</STRONG> ou <STRONG>adCmdTableDirect</STRONG> com <STRONG>CommandType</STRONG>. Esses valores podem ser usados somente como opções com os métodos <A href="open-method-ado-recordset.md">Open</A> e <A href="requery-method-ado.md">Requery</A> de um <A href="recordset-object-ado.md">Recordset</A>.</span><span class="sxs-lookup"><span data-stu-id="72616-p101">Do not use the <STRONG>CommandTypeEnum</STRONG> values of <STRONG>adCmdFile</STRONG> or <STRONG>adCmdTableDirect</STRONG> with <STRONG>CommandType</STRONG>. These values can only be used as options with the <A href="open-method-ado-recordset.md">Open</A> and <A href="requery-method-ado.md">Requery</A> methods of a <A href="recordset-object-ado.md">Recordset</A>.</span></span></P>



## <a name="remarks"></a><span data-ttu-id="72616-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="72616-109">Remarks</span></span>

<span data-ttu-id="72616-110">Use a propriedade **CommandType** para otimizar a avaliação da propriedade [CommandText](commandtext-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="72616-110">Use the **CommandType** property to optimize evaluation of the [CommandText](commandtext-property-ado.md) property.</span></span>

<span data-ttu-id="72616-p102">Se o valor da propriedade **CommandType** for igual a **adCmdUnknown** (o valor padrão), talvez você tenha uma diminuição do desempenho, pois o ADO deve fazer chamadas para o provedor para determinar se a propriedade **CommandText** é uma instrução SQL, um procedimento armazenado ou um nome de tabela. Se você souber que tipo de comando está usando, definir a propriedade **CommandType** instrui o ADO a ir diretamente para o código relevante. Se a propriedade **CommandType** não corresponder ao tipo de comando na propriedade **CommandText**, ocorrerá um erro quando você chamar o método [Open](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="72616-p102">If the **CommandType** property value equals **adCmdUnknown** (the default value), you may experience diminished performance because ADO must make calls to the provider to determine if the **CommandText** property is an SQL statement, a stored procedure, or a table name. If you know what type of command you're using, setting the **CommandType** property instructs ADO to go directly to the relevant code. If the **CommandType** property does not match the type of command in the **CommandText** property, an error occurs when you call the [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) method.</span></span>

