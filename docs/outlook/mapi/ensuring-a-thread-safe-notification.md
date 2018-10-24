---
title: Garantindo uma notificação livre de threads
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ad10b2ebd835b21f207fd43ecd8aebc7e1f475f4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585301"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="1b73c-103">Garantindo uma notificação livre de threads</span><span class="sxs-lookup"><span data-stu-id="1b73c-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="1b73c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1b73c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1b73c-105">Se seu cliente é executado em uma plataforma multithreaded, talvez você precise de garantia de que as chamadas para seus métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) ocorrerem em um determinado thread.</span><span class="sxs-lookup"><span data-stu-id="1b73c-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="1b73c-106">Porque as chamadas para **OnNotify** normalmente podem ocorrer em qualquer segmento, é possível receber notificações de threads inesperado e indesejado, levando a erros que são difíceis de depuração.</span><span class="sxs-lookup"><span data-stu-id="1b73c-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="1b73c-107">Garantir que as chamadas para **OnNotify** para uma notificação em particular sejam feitas no mesmo thread que foi usado para o **Advise** chamada, chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**.</span><span class="sxs-lookup"><span data-stu-id="1b73c-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="1b73c-108">\* \* \* \* HrThisThreadAdviseSink \* \* \* cria um novo objeto coletor de eventos advise seu objeto de coletor de eventos advise.</span><span class="sxs-lookup"><span data-stu-id="1b73c-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="1b73c-109">Passe este novo objeto na chamada a **Advise**.</span><span class="sxs-lookup"><span data-stu-id="1b73c-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="1b73c-110">Todos os clientes com o coletor de eventos advise objetos que podem não funcionar fora do contexto de um determinado thread sempre devem registrar aconselhe os objetos de coletor de eventos criados com **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="1b73c-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

