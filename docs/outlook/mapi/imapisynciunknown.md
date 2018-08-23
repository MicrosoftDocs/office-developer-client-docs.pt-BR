---
title: IMAPISync IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISync
api_type:
- COM
ms.assetid: c14d1012-f3d4-47eb-8a90-3160331f94e8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e2e7a3f9279485d862fac5bb6413b3d3eb1343e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589081"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="b7700-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7700-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="b7700-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b7700-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b7700-105">Oferece um mecanismo para sincronização de email em vez de usar a API de transporte.</span><span class="sxs-lookup"><span data-stu-id="b7700-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="b7700-106">Esta interface é exposto em um objeto de repositório.</span><span class="sxs-lookup"><span data-stu-id="b7700-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="b7700-107">Usando essa interface e [IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md), um provedor de transporte pode oferecer melhor progresso e mensagens de erro do que aqueles que aparecem na caixa de diálogo Enviar/receber no Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="b7700-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="b7700-108">A caixa de saída é ainda no armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="b7700-108">The outbox is still in the default store.</span></span> <span data-ttu-id="b7700-109">Outlook continuará usem as APIs de transporte para enviar emails, porque a mensagem de saída não pode ser no armazenamento externo.</span><span class="sxs-lookup"><span data-stu-id="b7700-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b7700-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="b7700-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="b7700-111">Provedores de armazenamento e de transporte</span><span class="sxs-lookup"><span data-stu-id="b7700-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="b7700-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b7700-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="b7700-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="b7700-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="b7700-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b7700-114">Called by:</span></span>  <br/> |<span data-ttu-id="b7700-115">Provedores de armazenamento e de transporte</span><span class="sxs-lookup"><span data-stu-id="b7700-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="b7700-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="b7700-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b7700-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="b7700-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b7700-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="b7700-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b7700-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="b7700-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="b7700-120">Implementado por provedores de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="b7700-120">Implemented by message store providers.</span></span> <span data-ttu-id="b7700-121">Esse método é chamado pelo Outlook 2010 e o Outlook 2013 para iniciar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="b7700-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b7700-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7700-122">See also</span></span>



[<span data-ttu-id="b7700-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7700-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="b7700-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="b7700-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

