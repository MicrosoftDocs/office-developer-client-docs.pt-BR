---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766879"
---
# <a name="iattach--imapiprop"></a><span data-ttu-id="ce37c-103">IAttach: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="ce37c-103">IAttach : IMAPIProp</span></span>

  
  
<span data-ttu-id="ce37c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ce37c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ce37c-105">Mantém e fornece acesso às propriedades de anexos em mensagens.</span><span class="sxs-lookup"><span data-stu-id="ce37c-105">Maintains and provides access to the properties of attachments in messages.</span></span> <span data-ttu-id="ce37c-106">A interface **IAttach** não possui exclusivos métodos sua própria conta.</span><span class="sxs-lookup"><span data-stu-id="ce37c-106">The **IAttach** interface has no unique methods of its own.</span></span> <span data-ttu-id="ce37c-107">Para obter mais informações sobre como usar os anexos, consulte [As tabelas de anexo](attachment-tables.md)e [Anexos de MAPI](mapi-attachments.md) .</span><span class="sxs-lookup"><span data-stu-id="ce37c-107">For more information about how to use attachments, see [MAPI Attachments](mapi-attachments.md) and [Attachment Tables](attachment-tables.md).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce37c-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ce37c-108">Header file:</span></span>  <br/> |<span data-ttu-id="ce37c-109">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ce37c-109">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ce37c-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="ce37c-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="ce37c-111">Objetos de anexo</span><span class="sxs-lookup"><span data-stu-id="ce37c-111">Attachment objects</span></span>  <br/> |
|<span data-ttu-id="ce37c-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ce37c-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="ce37c-113">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="ce37c-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="ce37c-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ce37c-114">Called by:</span></span>  <br/> |<span data-ttu-id="ce37c-115">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="ce37c-115">Client applications</span></span>  <br/> |
|<span data-ttu-id="ce37c-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ce37c-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ce37c-117">IID_IAttachment</span><span class="sxs-lookup"><span data-stu-id="ce37c-117">IID_IAttachment</span></span>  <br/> |
|<span data-ttu-id="ce37c-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ce37c-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="ce37c-119">LPATTACH</span><span class="sxs-lookup"><span data-stu-id="ce37c-119">LPATTACH</span></span>  <br/> |
|<span data-ttu-id="ce37c-120">Modelo de transação:</span><span class="sxs-lookup"><span data-stu-id="ce37c-120">Transaction model:</span></span>  <br/> |<span data-ttu-id="ce37c-121">Transacionadas</span><span class="sxs-lookup"><span data-stu-id="ce37c-121">Transacted</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ce37c-122">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="ce37c-122">Vtable order</span></span>

<span data-ttu-id="ce37c-123">Essa interface não tem quaisquer métodos exclusivos.</span><span class="sxs-lookup"><span data-stu-id="ce37c-123">This interface does not have any unique methods.</span></span>
  
|<span data-ttu-id="ce37c-124">**Propriedades necessárias**</span><span class="sxs-lookup"><span data-stu-id="ce37c-124">**Required properties**</span></span>|<span data-ttu-id="ce37c-125">**Access**</span><span class="sxs-lookup"><span data-stu-id="ce37c-125">**Access**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ce37c-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ce37c-126">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ce37c-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce37c-127">Read-only</span></span>  <br/> |
|<span data-ttu-id="ce37c-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ce37c-128">**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ce37c-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce37c-129">Read/write</span></span>  <br/> |
|<span data-ttu-id="ce37c-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ce37c-130">**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="ce37c-131">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ce37c-131">Read/write</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ce37c-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce37c-132">See also</span></span>



[<span data-ttu-id="ce37c-133">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ce37c-133">MAPI Interfaces</span></span>](mapi-interfaces.md)

