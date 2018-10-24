---
title: Evitar o uso de IStreamSetSize para estender um fluxo
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b6de594f-e331-4421-956b-86ee0b5518fe
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9245d4913c2832b8c942093e65cf088643a1947c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592077"
---
# <a name="avoiding-using-istreamsetsize-to-extend-a-stream"></a><span data-ttu-id="7afd5-103">Evitar usar IStream::SetSize para estender um fluxo</span><span class="sxs-lookup"><span data-stu-id="7afd5-103">Avoiding Using IStream::SetSize to Extend a Stream</span></span>

  
  
<span data-ttu-id="7afd5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7afd5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7afd5-105">Ao gravar fluxos, em alguns casos, é necessário ampliá-las porque seu tamanho inicial não é mais suficiente.</span><span class="sxs-lookup"><span data-stu-id="7afd5-105">When writing to streams, it is sometimes necessary to enlarge them because their initial size is no longer sufficient.</span></span> <span data-ttu-id="7afd5-106">Use o método OLE **IStream::Write** para realizar essa tarefa, em vez de **IStream::SetSize**.</span><span class="sxs-lookup"><span data-stu-id="7afd5-106">Use the OLE method **IStream::Write** to accomplish this rather than **IStream::SetSize**.</span></span> <span data-ttu-id="7afd5-107">**IStream::Write** automaticamente estende o fluxo, tornando \* \* IStream::SetSize \* \* desnecessárias.</span><span class="sxs-lookup"><span data-stu-id="7afd5-107">**IStream::Write** automatically extends the stream, making \*\* IStream::SetSize \*\* unnecessary.</span></span> <span data-ttu-id="7afd5-108">Chamar **IStream::Write** sem **IStream::SetSize** pode ser até três vezes mais rapidamente do que fazendo com que o **SetSize** chamada antes de **gravar**.</span><span class="sxs-lookup"><span data-stu-id="7afd5-108">Calling **IStream::Write** without **IStream::SetSize** can be up to three times faster than making the **SetSize** call prior to **Write**.</span></span>
  

