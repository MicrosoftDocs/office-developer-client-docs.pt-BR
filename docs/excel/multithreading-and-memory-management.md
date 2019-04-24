---
title: Gerenciamento de memória e multithreading
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f387d5ddb184c681ab5e005a6eb24058f6f52f9a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310385"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="ddf38-103">Gerenciamento de memória e multithreading</span><span class="sxs-lookup"><span data-stu-id="ddf38-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="ddf38-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="ddf38-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="ddf38-105">A manipulação adequada da memória é vital para a criação de suplementos XLL confiáveis para o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="ddf38-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="ddf38-106">Falha ao alocar buffers de memória apropriados e liberá-los quando eles não são mais necessários reduzem o desempenho, criam contenção de recursos e desestabilizam o Excel.</span><span class="sxs-lookup"><span data-stu-id="ddf38-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="ddf38-107">A partir do Microsoft Office Excel 2007, você pode configurar o Excel para usar até 1.024 threads simultâneos ao recalcular.</span><span class="sxs-lookup"><span data-stu-id="ddf38-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="ddf38-108">Em alguns casos, especialmente quando vários processadores estão disponíveis ou com funções definidas pelo usuário em execução em servidores em cluster, o multithreading pode melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="ddf38-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="ddf38-109">Os tópicos a seguir descrevem como gerenciar memória e threads em XLLs:</span><span class="sxs-lookup"><span data-stu-id="ddf38-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="ddf38-110">Gerenciamento de Memória no Excel</span><span class="sxs-lookup"><span data-stu-id="ddf38-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="ddf38-111">Multithreading e conTenção de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="ddf38-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="ddf38-112">Recálculo com vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="ddf38-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="ddf38-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddf38-113">See also</span></span>



[<span data-ttu-id="ddf38-114">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="ddf38-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

