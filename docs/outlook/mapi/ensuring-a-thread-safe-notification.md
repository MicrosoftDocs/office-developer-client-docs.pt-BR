---
title: Garantir uma notificação de thread-safe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d46ce99a-4d7f-45b0-ba21-154498c15775
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 88c58d14893f2ac561dc56441eb38b7f4bd0db32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424844"
---
# <a name="ensuring-a-thread-safe-notification"></a><span data-ttu-id="31ca7-103">Garantir uma notificação de thread-safe</span><span class="sxs-lookup"><span data-stu-id="31ca7-103">Ensuring a Thread-Safe Notification</span></span>

  
  
<span data-ttu-id="31ca7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31ca7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31ca7-105">Se seu cliente é executado em uma plataforma multithread, talvez você precise de garantia de que as chamadas para os métodos [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) ocorram em um thread específico.</span><span class="sxs-lookup"><span data-stu-id="31ca7-105">If your client runs on a multithreaded platform, you may need assurance that calls to your [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods occur on a particular thread.</span></span> <span data-ttu-id="31ca7-106">Como as chamadas \*\*\*\* para onnotificar normalmente podem ocorrer em qualquer thread, é possível receber notificações em threads indesejados e indesejados, levando a erros difíceis de depurar.</span><span class="sxs-lookup"><span data-stu-id="31ca7-106">Because calls to **OnNotify** can typically occur on any thread, it is possible to receive notifications on unexpected and unwanted threads, leading to errors that are difficult to debug.</span></span> 
  
<span data-ttu-id="31ca7-107">Para garantir que as chamadas \*\*\*\* para OnNotify para uma determinada notificação sejam feitas no mesmo thread que foi usado para a chamada de **aviso** , chame [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) antes de chamar **Advise**.</span><span class="sxs-lookup"><span data-stu-id="31ca7-107">To guarantee that calls to **OnNotify** for a particular notification are made on the same thread that was used for the **Advise** call, call [HrThisThreadAdviseSink](hrthisthreadadvisesink.md) before calling **Advise**.</span></span> <span data-ttu-id="31ca7-108">\* \* \* \* HrThisThreadAdviseSink \* \* \* \* cria um novo objeto de coletor de aviso do seu objeto de coletor de aviso.</span><span class="sxs-lookup"><span data-stu-id="31ca7-108">\*\* \*\*HrThisThreadAdviseSink\*\*\*\* creates a new advise sink object from your advise sink object.</span></span> <span data-ttu-id="31ca7-109">Passe este novo objeto na chamada para **Advise**.</span><span class="sxs-lookup"><span data-stu-id="31ca7-109">Pass this new object in the call to **Advise**.</span></span> <span data-ttu-id="31ca7-110">Todos os clientes com objetos de coletor de aviso que podem não funcionar fora do contexto de um determinado thread devem sempre registrar objetos de coletor de aviso criados com o **HrThisThreadAdviseSink**.</span><span class="sxs-lookup"><span data-stu-id="31ca7-110">All clients with advise sink objects that might not work outside the context of a particular thread should always register advise sink objects created with **HrThisThreadAdviseSink**.</span></span>
  

