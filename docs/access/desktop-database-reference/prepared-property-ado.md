---
title: Propriedade Prepared (ADO)
TOCTitle: Prepared property (ADO)
ms:assetid: 33becda2-faab-5000-8904-6ffd8c5805f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249105(v=office.15)
ms:contentKeyID: 48544116
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231161
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9541b2d584728c09ee852f628cdfc35f3d170f04
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718067"
---
# <a name="prepared-property-ado"></a><span data-ttu-id="8cdc7-102">Propriedade Prepared (ADO)</span><span class="sxs-lookup"><span data-stu-id="8cdc7-102">Prepared property (ADO)</span></span>


<span data-ttu-id="8cdc7-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="8cdc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8cdc7-104">Indica se uma versão compilada de um comando deve ser salva antes da execução.</span><span class="sxs-lookup"><span data-stu-id="8cdc7-104">Indicates whether to save a compiled version of a command before execution.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="8cdc7-105">Configurações e valores de retorno</span><span class="sxs-lookup"><span data-stu-id="8cdc7-105">Settings and return values</span></span>

<span data-ttu-id="8cdc7-106">Define ou retorna um valor **Boolean** que, se definido como **True**, indicará que o comando deve ser preparado.</span><span class="sxs-lookup"><span data-stu-id="8cdc7-106">Sets or returns a **Boolean** value that, if set to **True**, indicates that the command should be prepared.</span></span>

## <a name="remarks"></a><span data-ttu-id="8cdc7-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cdc7-107">Remarks</span></span>

<span data-ttu-id="8cdc7-p101">Utilize a propriedade **Prepared** para que o provedor salve uma versão preparada (ou compilada) da consulta especificada na propriedade [CommandText](commandtext-property-ado.md) antes da primeira execução de um objeto [Command](command-object-ado.md). Isto pode fazer com que a primeira execução do comando demore, mas depois que o provedor compilar um comando, ele utilizará a versão compilada do comando para quaisquer execuções subsequentes, melhorando o desempenho.</span><span class="sxs-lookup"><span data-stu-id="8cdc7-p101">Use the **Prepared** property to have the provider save a prepared (or compiled) version of the query specified in the [CommandText](commandtext-property-ado.md) property before a [Command](command-object-ado.md) object's first execution. This may slow a command's first execution, but once the provider compiles a command, the provider will use the compiled version of the command for any subsequent executions, which will result in improved performance.</span></span>

<span data-ttu-id="8cdc7-110">Se a propriedade for **False**, o provedor executará o objeto **Command** diretamente sem criar uma versão compilada.</span><span class="sxs-lookup"><span data-stu-id="8cdc7-110">If the property is **False**, the provider will execute the **Command** object directly without creating a compiled version.</span></span>

<span data-ttu-id="8cdc7-p102">Se o provedor não oferecer suporte à preparação do comando, ele poderá retornar um erro assim que essa propriedade for definida como **True**. Se não retornar um erro, ele simplesmente ignorará a solicitação para preparar o comando e definirá a propriedade **Prepared** como **False**.</span><span class="sxs-lookup"><span data-stu-id="8cdc7-p102">If the provider does not support command preparation, it may return an error as soon as this property is set to **True**. If it does not return an error, it simply ignores the request to prepare the command and sets the **Prepared** property to **False**.</span></span>

