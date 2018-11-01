---
title: Propriedade State (ADO)
TOCTitle: State property (ADO)
ms:assetid: ade0a50c-e2d8-23ac-4ea9-b012fedcd5db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249819(v=office.15)
ms:contentKeyID: 48547053
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231176
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d8ea3738465ed9bfc10cbabdf355036f7c160f66
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886610"
---
# <a name="state-property-ado"></a><span data-ttu-id="b7b6b-102">Propriedade State (ADO)</span><span class="sxs-lookup"><span data-stu-id="b7b6b-102">State property (ADO)</span></span>


<span data-ttu-id="b7b6b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="b7b6b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b7b6b-104">Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="b7b6b-105">Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="b7b6b-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="b7b6b-106">Return value</span></span>

<span data-ttu-id="b7b6b-p101">Retorna um valor **Long** que pode ser um valor [ObjectStateEnum](objectstateenum.md). O valor padrão é **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-p101">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value. The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7b6b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7b6b-109">Remarks</span></span>

<span data-ttu-id="b7b6b-110">Você pode utilizar a propriedade **State** para identificar o estado atual de um determinado objeto em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="b7b6b-p102">A propriedade **State** do objeto pode ter uma combinação de valores. Por exemplo, se uma instrução estiver sendo executada, essa propriedade terá uma combinação de valores de **adStateOpen** e **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="b7b6b-113">A propriedade **State** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b7b6b-113">The **State** property is read-only.</span></span>

