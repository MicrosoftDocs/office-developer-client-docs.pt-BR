---
title: Propriedade canônica PidTagRemoteValidateOk
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRemoteValidateOk
api_type:
- COM
ms.assetid: e336d2ec-57cb-4d08-bd6e-330ef7d9939e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8b5c9e5bb2aa915d4b76d9998baaf504e7929b78
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424221"
---
# <a name="pidtagremotevalidateok-canonical-property"></a><span data-ttu-id="c813c-103">Propriedade canônica PidTagRemoteValidateOk</span><span class="sxs-lookup"><span data-stu-id="c813c-103">PidTagRemoteValidateOk Canonical Property</span></span>

  
  
<span data-ttu-id="c813c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c813c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c813c-105">Essa propriedade conterá TRUE se o visualizador remoto tiver permissão para chamar o [método IMAPIStatus::ValidateState.](imapistatus-validatestate.md)</span><span class="sxs-lookup"><span data-stu-id="c813c-105">This property contains TRUE if the remote viewer is allowed to call the [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c813c-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c813c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c813c-107">PR_REMOTE_VALIDATE_OK</span><span class="sxs-lookup"><span data-stu-id="c813c-107">PR_REMOTE_VALIDATE_OK</span></span>  <br/> |
|<span data-ttu-id="c813c-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c813c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c813c-109">0x3E0D</span><span class="sxs-lookup"><span data-stu-id="c813c-109">0x3E0D</span></span>  <br/> |
|<span data-ttu-id="c813c-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c813c-110">Data type:</span></span>  <br/> |<span data-ttu-id="c813c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="c813c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="c813c-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c813c-112">Area:</span></span>  <br/> |<span data-ttu-id="c813c-113">MAPI Status</span><span class="sxs-lookup"><span data-stu-id="c813c-113">MAPI Status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c813c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c813c-114">Remarks</span></span>

<span data-ttu-id="c813c-115">Essa propriedade aparece na tabela de status e oferece algum controle sobre o desempenho do transporte.</span><span class="sxs-lookup"><span data-stu-id="c813c-115">This property appears in the status table and offers some control over transport performance.</span></span> <span data-ttu-id="c813c-116">Ele pode ser considerado como outra maneira de direcionar o visualizador remoto para ocioso.</span><span class="sxs-lookup"><span data-stu-id="c813c-116">It can be considered as another way of directing the remote viewer to idle.</span></span> <span data-ttu-id="c813c-117">Quando definido como TRUE, o visualizador remoto pode chamar **IMAPIStatus::ValidateState** com a frequência desejada.</span><span class="sxs-lookup"><span data-stu-id="c813c-117">When it is set to TRUE, the remote viewer can call **IMAPIStatus::ValidateState** as often as desired.</span></span> <span data-ttu-id="c813c-118">Um valor FALSO indica que o visualizador remoto não pode fazer mais chamadas.</span><span class="sxs-lookup"><span data-stu-id="c813c-118">A value of FALSE indicates that the remote viewer cannot make any more calls.</span></span> 
  
<span data-ttu-id="c813c-119">O provedor de transporte geralmente define essa propriedade dinamicamente, definindo o valor como FALSE para desabilitar chamadas adicionais quando o provedor de transporte tiver uma quantidade suficiente de processamento para executar.</span><span class="sxs-lookup"><span data-stu-id="c813c-119">The transport provider usually sets this property dynamically, by setting the value to FALSE to disable additional calls when the transport provider has a sufficient amount of processing to perform.</span></span> <span data-ttu-id="c813c-120">Quando o provedor de transporte é feito, ele define o valor como TRUE para permitir que o aplicativo cliente faça chamadas **IMAPIStatus::ValidateState.**</span><span class="sxs-lookup"><span data-stu-id="c813c-120">When the transport provider is done, it then sets the value to TRUE to allow the client application to make further **IMAPIStatus::ValidateState** calls.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c813c-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c813c-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c813c-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="c813c-122">Header files</span></span>

<span data-ttu-id="c813c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c813c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c813c-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c813c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c813c-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c813c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c813c-126">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="c813c-126">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c813c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c813c-127">See also</span></span>



[<span data-ttu-id="c813c-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c813c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c813c-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c813c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c813c-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c813c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c813c-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c813c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

