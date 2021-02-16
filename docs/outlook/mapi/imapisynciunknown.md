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
ms.openlocfilehash: 4d46152136f3806c79f0dd454ed9fd41fc845721
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405588"
---
# <a name="imapisync--iunknown"></a><span data-ttu-id="e3977-103">IMAPISync : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3977-103">IMAPISync : IUnknown</span></span>

  
  
<span data-ttu-id="e3977-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3977-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3977-105">Fornece um mecanismo para sincronizar emails em vez de usar a API de Transporte.</span><span class="sxs-lookup"><span data-stu-id="e3977-105">Provides a mechanism for synchronizing email instead of using the Transport API.</span></span> <span data-ttu-id="e3977-106">Essa interface é exposta em um objeto store.</span><span class="sxs-lookup"><span data-stu-id="e3977-106">This interface is exposed on a store object.</span></span> <span data-ttu-id="e3977-107">Usando essa interface e [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), um provedor de transporte pode fornecer mensagens de erro e progresso melhores do que aquelas que aparecem na caixa de diálogo Enviar/Receber no Microsoft Outlook.</span><span class="sxs-lookup"><span data-stu-id="e3977-107">By using this interface and [IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md), a transport provider can provide better progress and error messages than those that appear in the Send/Receive dialog in Microsoft Outlook.</span></span>
  
<span data-ttu-id="e3977-108">A caixa de saída ainda está no armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="e3977-108">The outbox is still in the default store.</span></span> <span data-ttu-id="e3977-109">O Outlook continuará a usar as APIs de Transporte para enviar emails porque a mensagem de saída não pode estar no armazenamento externo.</span><span class="sxs-lookup"><span data-stu-id="e3977-109">Outlook will continue to use the Transport APIs to send mail because the outgoing message cannot be in the external store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e3977-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="e3977-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="e3977-111">Provedores de transporte e loja</span><span class="sxs-lookup"><span data-stu-id="e3977-111">Store and transport providers</span></span>  <br/> |
|<span data-ttu-id="e3977-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="e3977-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="e3977-113">Outlook</span><span class="sxs-lookup"><span data-stu-id="e3977-113">Outlook</span></span>  <br/> |
|<span data-ttu-id="e3977-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="e3977-114">Called by:</span></span>  <br/> |<span data-ttu-id="e3977-115">Provedores de Transporte e Loja</span><span class="sxs-lookup"><span data-stu-id="e3977-115">Store and Transport providers</span></span>  <br/> |
|<span data-ttu-id="e3977-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="e3977-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e3977-117">IID_IMAPISync</span><span class="sxs-lookup"><span data-stu-id="e3977-117">IID_IMAPISync</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e3977-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="e3977-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e3977-119">SynchronizeInBackground</span><span class="sxs-lookup"><span data-stu-id="e3977-119">SynchronizeInBackground</span></span>](imapisyncsynchronizeinbackground.md) <br/> |<span data-ttu-id="e3977-120">Implementado pelos provedores de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e3977-120">Implemented by message store providers.</span></span> <span data-ttu-id="e3977-121">Esse método é chamado pelo Outlook 2010 e pelo Outlook 2013 para iniciar a sincronização.</span><span class="sxs-lookup"><span data-stu-id="e3977-121">This method is called by Outlook 2010 and Outlook 2013 to start synchronization.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3977-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3977-122">See also</span></span>



[<span data-ttu-id="e3977-123">IMAPISyncProgressCallback : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e3977-123">IMAPISyncProgressCallback : IUnknown</span></span>](imapisyncprogresscallbackiunknown.md)


[<span data-ttu-id="e3977-124">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e3977-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

