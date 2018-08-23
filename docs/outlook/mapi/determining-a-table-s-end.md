---
title: Determinar o fim de uma tabela
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c879e972-05f4-4716-8fc2-db5b22f34ca8
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: f9979baf144b6106adcec416ee04439404e05d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576341"
---
# <a name="determining-a-tables-end"></a><span data-ttu-id="44770-103">Determinar o fim de uma tabela</span><span class="sxs-lookup"><span data-stu-id="44770-103">Determining a Table's End</span></span>

  
  
<span data-ttu-id="44770-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44770-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="44770-105">Um erro comum é pressupõem que o fim da tabela foi alcançado quando:</span><span class="sxs-lookup"><span data-stu-id="44770-105">A common error is to assume that the end of the table has been reached when:</span></span> 
  
- <span data-ttu-id="44770-106">[IMAPITable:: QueryRows](imapitable-queryrows.md) foi chamado em um loop, com o fim do loop determinado pela contagem de linhas retornada pela [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span><span class="sxs-lookup"><span data-stu-id="44770-106">[IMAPITable::QueryRows](imapitable-queryrows.md) has been called in a loop, with the end of the loop determined by the row count returned by [IMAPITable::GetRowCount](imapitable-getrowcount.md).</span></span> <span data-ttu-id="44770-107">A contagem de **GetRowCount** retorna nem sempre representam o número exato de linhas da tabela. é uma contagem aproximada.</span><span class="sxs-lookup"><span data-stu-id="44770-107">The count that **GetRowCount** returns does not always represent the exact number of rows in the table; it is an approximate count.</span></span> 
    
- <span data-ttu-id="44770-108">**QueryRows** tenha sido chamado com um número fixo de linhas e menos linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="44770-108">**QueryRows** has been called with a fixed number of rows and fewer rows are returned.</span></span> <span data-ttu-id="44770-109">É não até **QueryRows** retorna uma linha definidas com uma contagem de linhas igual a zero não existem mais linhas para recuperar.</span><span class="sxs-lookup"><span data-stu-id="44770-109">It is not until **QueryRows** returns a row set with a row count equal to zero that there are no more rows to retrieve.</span></span> 
    
> [!IMPORTANT]
> <span data-ttu-id="44770-110">A única vez que um chamador pode assumir que o cursor é posicionado no final da tabela para uma contagem de linha positivo ou no início da tabela para uma contagem de linha negativo é quando o valor S_OK e zero linhas são retornadas.</span><span class="sxs-lookup"><span data-stu-id="44770-110">The only time that a caller can assume that the cursor is positioned at the end of the table for a positive row count or at the beginning of the table for a negative row count is when the value S_OK and zero rows are returned.</span></span> <span data-ttu-id="44770-111">O valor E_NOT_FOUND nunca será retornado.</span><span class="sxs-lookup"><span data-stu-id="44770-111">The value MAPI_E_NOT_FOUND is never returned.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="44770-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="44770-112">See also</span></span>



[<span data-ttu-id="44770-113">Tabelas MAPI</span><span class="sxs-lookup"><span data-stu-id="44770-113">MAPI Tables</span></span>](mapi-tables.md)

