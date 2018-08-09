---
title: Vários threads e gerenciamento de memória
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f7e052a-4270-4b83-b1ed-feabf6dbeaa2
description: 'Aplica-se a: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f5495648c9012b0e028358037090f7e10ef5219
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765423"
---
# <a name="multithreading-and-memory-management"></a><span data-ttu-id="862fb-103">Vários threads e gerenciamento de memória</span><span class="sxs-lookup"><span data-stu-id="862fb-103">Multithreading and Memory Management</span></span>

 <span data-ttu-id="862fb-104">**Aplica-se a**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="862fb-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="862fb-105">Manipulação adequada de memória é vital para a criação de suplementos XLL confiáveis para o Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="862fb-105">Proper handling of memory is vital to creating reliable XLL add-ins for Microsoft Excel.</span></span> <span data-ttu-id="862fb-106">Falha ao alocar buffers de memória apropriado e liberá-los quando eles não são mais necessários reduz o desempenho, cria contenção de recursos e destabilizes Excel.</span><span class="sxs-lookup"><span data-stu-id="862fb-106">Failure to allocate appropriate memory buffers and free them when they are no longer needed reduces performance, creates resource contention, and destabilizes Excel.</span></span>
  
<span data-ttu-id="862fb-107">A partir do Microsoft Office Excel 2007, você pode configurar o Excel para usar até 1.024 segmentos simultâneos durante o recálculo.</span><span class="sxs-lookup"><span data-stu-id="862fb-107">Beginning with Microsoft Office Excel 2007, you can configure Excel to use up to 1,024 concurrent threads when recalculating.</span></span> <span data-ttu-id="862fb-108">Em alguns casos, especialmente quando vários processadores estão disponíveis ou com definidas pelo usuário funções em execução em servidores clusterizados multithreading podem melhorar o desempenho.</span><span class="sxs-lookup"><span data-stu-id="862fb-108">In some cases, especially when multiple processors are available or with user-defined functions running on clustered servers, multithreading can improve performance.</span></span>
  
<span data-ttu-id="862fb-109">Os tópicos a seguir descrevem como gerenciar memória e threads em XLLs:</span><span class="sxs-lookup"><span data-stu-id="862fb-109">The following topics describe how to manage memory and threads in XLLs:</span></span>
  
- [<span data-ttu-id="862fb-110">Gerenciamento de memória no Excel</span><span class="sxs-lookup"><span data-stu-id="862fb-110">Memory Management in Excel</span></span>](memory-management-in-excel.md)
    
- [<span data-ttu-id="862fb-111">Vários threads e contenção da memória no Excel</span><span class="sxs-lookup"><span data-stu-id="862fb-111">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
    
- [<span data-ttu-id="862fb-112">Recálculo do vários threads no Excel</span><span class="sxs-lookup"><span data-stu-id="862fb-112">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
    
## <a name="see-also"></a><span data-ttu-id="862fb-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="862fb-113">See also</span></span>



[<span data-ttu-id="862fb-114">Desenvolvimento de XLLs do Excel</span><span class="sxs-lookup"><span data-stu-id="862fb-114">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

