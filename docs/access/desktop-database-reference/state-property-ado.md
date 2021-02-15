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
localization_priority: Normal
ms.openlocfilehash: 0bce3f87a6530315a128396fe0e4de5390e0f47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308530"
---
# <a name="state-property-ado"></a><span data-ttu-id="68b34-102">Propriedade State (ADO)</span><span class="sxs-lookup"><span data-stu-id="68b34-102">State property (ADO)</span></span>


<span data-ttu-id="68b34-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68b34-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68b34-104">Indica todos os objetos aplicáveis, independentemente de seu estado: aberto ou fechado.</span><span class="sxs-lookup"><span data-stu-id="68b34-104">Indicates for all applicable objects whether the state of the object is open or closed.</span></span>

<span data-ttu-id="68b34-105">Indica todos os objetos aplicáveis que executam um método assíncrono, independentemente de seu estado atual: conexão, execução ou recuperação.</span><span class="sxs-lookup"><span data-stu-id="68b34-105">Indicates for all applicable objects executing an asynchronous method, whether the current state of the object is connecting, executing, or retrieving.</span></span>

## <a name="return-value"></a><span data-ttu-id="68b34-106">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="68b34-106">Return value</span></span>

<span data-ttu-id="68b34-107">Retorna um valor **Long** que pode ser um valor [ObjectStateEnum](objectstateenum.md).</span><span class="sxs-lookup"><span data-stu-id="68b34-107">Returns a **Long** value that can be an [ObjectStateEnum](objectstateenum.md) value.</span></span> <span data-ttu-id="68b34-108">O valor padrão é **adStateClosed**.</span><span class="sxs-lookup"><span data-stu-id="68b34-108">The default value is **adStateClosed**.</span></span>

## <a name="remarks"></a><span data-ttu-id="68b34-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="68b34-109">Remarks</span></span>

<span data-ttu-id="68b34-110">Você pode utilizar a propriedade **State** para identificar o estado atual de um determinado objeto em qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="68b34-110">You can use the **State** property to determine the current state of a given object at any time.</span></span>

<span data-ttu-id="68b34-p102">A propriedade **State** do objeto pode ter uma combinação de valores. Por exemplo, se uma instrução estiver sendo executada, essa propriedade terá uma combinação de valores de **adStateOpen** e **adStateExecuting**.</span><span class="sxs-lookup"><span data-stu-id="68b34-p102">The object's **State** property can have a combination of values. For example, if a statement is executing, this property will have a combined value of **adStateOpen** and **adStateExecuting**.</span></span>

<span data-ttu-id="68b34-113">A propriedade **State** é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="68b34-113">The **State** property is read-only.</span></span>

