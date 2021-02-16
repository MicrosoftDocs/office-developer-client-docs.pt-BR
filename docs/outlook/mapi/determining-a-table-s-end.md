---
title: Determinando o final de uma tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 28892e2d351b8dc9aa864c9eff52c94bb0f20e8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420084"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="f1df6-103">Determinando o final de uma tabela</span><span class="sxs-lookup"><span data-stu-id="f1df6-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="f1df6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f1df6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="f1df6-105">Um erro comum é presumir que o final da tabela foi atingido quando:</span><span class="sxs-lookup"><span data-stu-id="f1df6-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="f1df6-106">[IMAPITable::QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o final do loop determinado pela contagem de linhas retornada por [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="f1df6-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="f1df6-107">A contagem **retornada por GetRowCount** nem sempre representa o número exato de linhas na tabela; é uma contagem aproximada.</span><span class="sxs-lookup"><span data-stu-id="f1df6-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="f1df6-108">**QueryRows** foi chamado com um número fixo de linhas e menos linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="f1df6-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="f1df6-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span><span class="sxs-lookup"><span data-stu-id="f1df6-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="f1df6-110">A única vez que um chamador pode assumir que o cursor está posicionado no final da tabela para uma contagem de linhas positiva ou no início da tabela para uma contagem de linhas negativas é quando o valor S_OK e zero linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="f1df6-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="f1df6-111">O valor MAPI_E_NOT_FOUND é retornado.</span><span class="sxs-lookup"><span data-stu-id="f1df6-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f1df6-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1df6-112">See also</span></span>



[<span data-ttu-id="f1df6-113">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="f1df6-113">MAPI Tables</span></span>](mapi-tables.md)

