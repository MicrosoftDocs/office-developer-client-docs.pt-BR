---
title: IMAPISyncProgressCallback IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback
api_type:
- COM
ms.assetid: 146b5e36-8d73-4949-9fed-1074f707423d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54f61eb1bf111601e8b2c889b0d2890d0c10d63b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341234"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="f9bde-103">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9bde-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="f9bde-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9bde-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9bde-105">Passa o provedor de repositório como um campo na estrutura MAPISIB durante uma chamada para [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="f9bde-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="f9bde-106">O provedor de repositório usa essa interface para fornecer comentários ao Microsoft Outlook sobre o status da sincronização.</span><span class="sxs-lookup"><span data-stu-id="f9bde-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f9bde-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f9bde-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="f9bde-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="f9bde-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f9bde-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="f9bde-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="f9bde-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f9bde-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9bde-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="f9bde-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="f9bde-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f9bde-112">Called by:</span></span>  <br/> |<span data-ttu-id="f9bde-113">Provedores de repositório</span><span class="sxs-lookup"><span data-stu-id="f9bde-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="f9bde-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="f9bde-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f9bde-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="f9bde-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f9bde-116">Vtable order</span><span class="sxs-lookup"><span data-stu-id="f9bde-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f9bde-117">Progress</span><span class="sxs-lookup"><span data-stu-id="f9bde-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="f9bde-118">O provedor de repositório chama periodicamente essa função para atualizar o status na caixa de diálogo enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="f9bde-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="f9bde-119">Error</span><span class="sxs-lookup"><span data-stu-id="f9bde-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="f9bde-120">Se forem encontrados erros durante a sincronização, o provedor de repositório chamará essa função para fornecer detalhes que são exibidos na caixa de diálogo enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="f9bde-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="f9bde-121">Feito</span><span class="sxs-lookup"><span data-stu-id="f9bde-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="f9bde-122">O provedor de repositório chama essa função para informar ao Outlook que a sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="f9bde-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9bde-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9bde-123">See also</span></span>



[<span data-ttu-id="f9bde-124">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9bde-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="f9bde-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f9bde-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

