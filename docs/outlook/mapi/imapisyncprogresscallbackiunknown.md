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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: bce70d891bc33dcddb94fc05992c09991c6cdc63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767310"
---
# <a name="imapisyncprogresscallback--iunknown"></a><span data-ttu-id="9d2f7-103">IMAPISyncProgressCallback: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d2f7-103">IMAPISyncProgressCallback : IUnknown</span></span>

  
  
<span data-ttu-id="9d2f7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d2f7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d2f7-105">Passa o provedor de armazenamento como um campo na estrutura MAPISIB durante uma chamada para [IMAPISync: SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span><span class="sxs-lookup"><span data-stu-id="9d2f7-105">Passes the store provider as a field on the MAPISIB structure during a call to [IMAPISync : SynchronizeInBackground](imapisyncsynchronizeinbackground.md).</span></span> <span data-ttu-id="9d2f7-106">O provedor de armazenamento usa essa interface para fornecer comentários para o Microsoft Outlook sobre o status da sincronização.</span><span class="sxs-lookup"><span data-stu-id="9d2f7-106">The store provider uses this interface to provide feedback to Microsoft Outlook about the status of the synchronization.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9d2f7-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9d2f7-107">Header file:</span></span>  <br/> ||
|<span data-ttu-id="9d2f7-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="9d2f7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9d2f7-109">Outlook</span><span class="sxs-lookup"><span data-stu-id="9d2f7-109">Outlook</span></span>  <br/> |
|<span data-ttu-id="9d2f7-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9d2f7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9d2f7-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="9d2f7-111">Outlook</span></span>  <br/> |
|<span data-ttu-id="9d2f7-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9d2f7-112">Called by:</span></span>  <br/> |<span data-ttu-id="9d2f7-113">Provedores de armazenamento</span><span class="sxs-lookup"><span data-stu-id="9d2f7-113">Store providers</span></span>  <br/> |
|<span data-ttu-id="9d2f7-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9d2f7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9d2f7-115">IID_IMAPISyncProgressCallback</span><span class="sxs-lookup"><span data-stu-id="9d2f7-115">IID_IMAPISyncProgressCallback</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9d2f7-116">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="9d2f7-116">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9d2f7-117">Progress</span><span class="sxs-lookup"><span data-stu-id="9d2f7-117">Progress</span></span>](imapisyncprogresscallback-progress.md) <br/> |<span data-ttu-id="9d2f7-118">O provedor de armazenamento periodicamente chama esta função para atualizar o status na caixa de diálogo Enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="9d2f7-118">The store provider periodically calls this function to update the status in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="9d2f7-119">Erro</span><span class="sxs-lookup"><span data-stu-id="9d2f7-119">Error</span></span>](imapisyncprogresscallback-error.md) <br/> |<span data-ttu-id="9d2f7-120">Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama esta função para fornecer detalhes que são exibidos na caixa de diálogo Enviar/receber.</span><span class="sxs-lookup"><span data-stu-id="9d2f7-120">If errors are encountered during synchronization, the store provider calls this function to provide details that are displayed in the Send/Receive dialog.</span></span>  <br/> |
|[<span data-ttu-id="9d2f7-121">Feito</span><span class="sxs-lookup"><span data-stu-id="9d2f7-121">Done</span></span>](imapisyncprogresscallback-done.md) <br/> |<span data-ttu-id="9d2f7-122">O provedor de armazenamento chama esta função para informe ao Outlook sincronização foi concluída.</span><span class="sxs-lookup"><span data-stu-id="9d2f7-122">The store provider calls this function to inform Outlook that synchronization has completed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d2f7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d2f7-123">See also</span></span>



[<span data-ttu-id="9d2f7-124">IMAPISync: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d2f7-124">IMAPISync : IUnknown</span></span>](imapisynciunknown.md)


[<span data-ttu-id="9d2f7-125">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9d2f7-125">MAPI Interfaces</span></span>](mapi-interfaces.md)

