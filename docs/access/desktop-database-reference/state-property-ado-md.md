---
title: Propriedade State (ADO MD)
TOCTitle: State property (ADO MD)
ms:assetid: 4df09f45-9b62-33ce-b4ed-230e41eaac7a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249249(v=office.15)
ms:contentKeyID: 48544744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 051a9f0cc50ae3a60edb033f6807f72fc0688976
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306360"
---
# <a name="state-property-ado-md"></a><span data-ttu-id="daf46-102">Propriedade State (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="daf46-102">State property (ADO MD)</span></span>


<span data-ttu-id="daf46-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="daf46-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="daf46-104">Indica o estado atual do conjunto de células.</span><span class="sxs-lookup"><span data-stu-id="daf46-104">Indicates the current state of the cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="daf46-105">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="daf46-105">Return values</span></span>

<span data-ttu-id="daf46-106">Retorna um inteiro **Long** que indica a condição atual do objeto [Cellset](cellset-object-ado-md.md) e é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="daf46-106">Returns a **Long** integer indicating the current condition of the [Cellset](cellset-object-ado-md.md) object and is read-only.</span></span> <span data-ttu-id="daf46-107">Os seguintes valores são válidos: **adStateClosed** (0) e **adStateOpen** (1).</span><span class="sxs-lookup"><span data-stu-id="daf46-107">The following values are valid: **adStateClosed** (0) and **adStateOpen** (1).</span></span>

## <a name="remarks"></a><span data-ttu-id="daf46-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="daf46-108">Remarks</span></span>

<span data-ttu-id="daf46-p102">Para usar os nomes da constante [ObjectStateEnum](objectstateenum.md), a biblioteca de tipos ADO deve ser referenciada em seu projeto. Para obter mais informações, consulte [Usando o ADO com o ADO MD](using-ado-with-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="daf46-p102">To use the [ObjectStateEnum](objectstateenum.md) constant names, you must have the ADO type library referenced in your project. See [Using ADO with ADO MD](using-ado-with-ado-md.md) for more information.</span></span>

