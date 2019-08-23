---
title: Evitar determinados métodos na inicialização
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7bb86fc8-d1ae-4937-9919-86c3a0f5651d
description: 'Última modificação: 07 de dezembro de 2015'
ms.openlocfilehash: 21aafebefcb7e10e6ba432f2eb3cc5dc04978c20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318085"
---
# <a name="avoiding-certain-methods-at-startup"></a><span data-ttu-id="116ac-103">Evitar determinados métodos na inicialização</span><span class="sxs-lookup"><span data-stu-id="116ac-103">Avoiding Certain Methods at Startup</span></span>

 
  
<span data-ttu-id="116ac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="116ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="116ac-105">Para melhorar o desempenho no momento da inicialização, evite fazer seguintes chamadas:</span><span class="sxs-lookup"><span data-stu-id="116ac-105">To improve performance at startup time, avoid making the following calls:</span></span>
  
- [<span data-ttu-id="116ac-106">IMAPISession::EnumAdrTypes</span><span class="sxs-lookup"><span data-stu-id="116ac-106">IMAPISession::EnumAdrTypes</span></span>](imapisession-enumadrtypes.md)
    
- [<span data-ttu-id="116ac-107">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="116ac-107">IMAPISession::GetStatusTable</span></span>](imapisession-getstatustable.md)
    
- [<span data-ttu-id="116ac-108">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="116ac-108">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
    
- [<span data-ttu-id="116ac-109">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="116ac-109">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)
    
- [<span data-ttu-id="116ac-110">IMAPIStatus::ValidateState</span><span class="sxs-lookup"><span data-stu-id="116ac-110">IMAPIStatus::ValidateState</span></span>](imapistatus-validatestate.md)
    
<span data-ttu-id="116ac-111">Chamadas para **IMAPIStatus::ValidateState** afetam o desempenho somente quando feitas no spooler MAPI ou no subsistema MAPI.</span><span class="sxs-lookup"><span data-stu-id="116ac-111">The call to **IMAPIStatus::ValidateState** affects performance only when made on either the MAPI spooler or the MAPI subsystem.</span></span> <span data-ttu-id="116ac-112">O motivo pelo qual esses métodos reduzem a velocidade do processo de inicialização é porque eles não podem se concluir até que o spooler MAPI termine suas tarefas de inicialização.</span><span class="sxs-lookup"><span data-stu-id="116ac-112">The reason that these methods slow startup processing is because they cannot complete until the MAPI spooler has finished its startup tasks.</span></span> 
  
<span data-ttu-id="116ac-113">Você deve evitar pesquisar o repositório de mensagens no momento da inicialização.</span><span class="sxs-lookup"><span data-stu-id="116ac-113">You should also avoid searching the message store at startup time.</span></span> <span data-ttu-id="116ac-114">Verifique sua chamada [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) quando to processo de inicialização for concluído.</span><span class="sxs-lookup"><span data-stu-id="116ac-114">Make your [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) call when startup processing has finished.</span></span> 
  

