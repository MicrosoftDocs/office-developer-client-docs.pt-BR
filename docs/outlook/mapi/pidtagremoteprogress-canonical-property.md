---
title: Propriedade canônica PidTagRemoteProgress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteProgress
api_type:
- COM
ms.assetid: 01cae79e-5b56-4cd4-83a6-f0956ff539fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a5a9d0796bc92514ae6d990b7328364b85bc55cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335431"
---
# <a name="pidtagremoteprogress-canonical-property"></a><span data-ttu-id="c2380-103">Propriedade canônica PidTagRemoteProgress</span><span class="sxs-lookup"><span data-stu-id="c2380-103">PidTagRemoteProgress Canonical Property</span></span>

  
  
<span data-ttu-id="c2380-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2380-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2380-105">Esta propriedade contém um número que indica o status de uma transferência remota.</span><span class="sxs-lookup"><span data-stu-id="c2380-105">This property contains a number that indicates the status of a remote transfer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c2380-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c2380-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c2380-107">PR_REMOTE_PROGRESS</span><span class="sxs-lookup"><span data-stu-id="c2380-107">PR_REMOTE_PROGRESS</span></span>  <br/> |
|<span data-ttu-id="c2380-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c2380-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c2380-109">0x3E0B</span><span class="sxs-lookup"><span data-stu-id="c2380-109">0x3E0B</span></span>  <br/> |
|<span data-ttu-id="c2380-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c2380-110">Data type:</span></span>  <br/> |<span data-ttu-id="c2380-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c2380-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c2380-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c2380-112">Area:</span></span>  <br/> |<span data-ttu-id="c2380-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="c2380-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c2380-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2380-114">Remarks</span></span>

<span data-ttu-id="c2380-115">Se nenhuma transferência estiver em andamento, esta propriedade deverá ser definida como 1.</span><span class="sxs-lookup"><span data-stu-id="c2380-115">If no transfer is in progress, this property should be set to 1.</span></span> <span data-ttu-id="c2380-116">Se uma transferência estiver em andamento, ela deverá ser definida como um valor de 0 a 100, indicando a porcentagem de conclusão da transferência.</span><span class="sxs-lookup"><span data-stu-id="c2380-116">If a transfer is in progress, it should be set to a value from 0 to 100 indicating the transfer's percent of completion.</span></span>
  
<span data-ttu-id="c2380-117">O texto associado ao código de status numérico aparece na propriedade **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c2380-117">The text associated with the numeric status code appears in the **PR_REMOTE_PROGRESS_TEXT** ([PidTagRemoteProgressText](pidtagremoteprogresstext-canonical-property.md)) property.</span></span>
  
<span data-ttu-id="c2380-118">Os seguintes sinalizadores podem ser definidos para esta propriedade:</span><span class="sxs-lookup"><span data-stu-id="c2380-118">The following flags can be set for this property:</span></span>
  
<span data-ttu-id="c2380-119">MSGSTATUS_REMOTE_DELETE</span><span class="sxs-lookup"><span data-stu-id="c2380-119">MSGSTATUS_REMOTE_DELETE</span></span>
  
> <span data-ttu-id="c2380-120">A transferência de mensagem é excluída.</span><span class="sxs-lookup"><span data-stu-id="c2380-120">The message transfer is deleted.</span></span>
    
<span data-ttu-id="c2380-121">MSGSTATUS_REMOTE_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="c2380-121">MSGSTATUS_REMOTE_DOWNLOAD</span></span>
  
> <span data-ttu-id="c2380-122">A transferência de mensagem está em andamento.</span><span class="sxs-lookup"><span data-stu-id="c2380-122">The message transfer is in progress.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="c2380-123">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c2380-123">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c2380-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c2380-124">Header files</span></span>

<span data-ttu-id="c2380-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c2380-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="c2380-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c2380-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="c2380-127">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c2380-127">Mapitags.h</span></span>
  
> <span data-ttu-id="c2380-128">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c2380-128">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c2380-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c2380-129">See also</span></span>



[<span data-ttu-id="c2380-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c2380-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c2380-131">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c2380-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c2380-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c2380-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c2380-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c2380-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

