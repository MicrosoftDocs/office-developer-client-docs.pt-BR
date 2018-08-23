---
title: Propriedade canônica PidTagProviderSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderSubmitTime
api_type:
- COM
ms.assetid: 9e5161d9-fefe-4a12-b7f7-5600f1d2e95b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e08b56fcfea38bf65e8628acfa481716554e2c01
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571609"
---
# <a name="pidtagprovidersubmittime-canonical-property"></a><span data-ttu-id="b23f3-103">Propriedade canônica PidTagProviderSubmitTime</span><span class="sxs-lookup"><span data-stu-id="b23f3-103">PidTagProviderSubmitTime Canonical Property</span></span>

  
  
<span data-ttu-id="b23f3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b23f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b23f3-105">Contém a data e hora de que um provedor de transporte passada uma mensagem para seu sistema de mensagens subjacente.</span><span class="sxs-lookup"><span data-stu-id="b23f3-105">Contains the date and time a transport provider passed a message to its underlying messaging system.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b23f3-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="b23f3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b23f3-107">PR_PROVIDER_SUBMIT_TIME</span><span class="sxs-lookup"><span data-stu-id="b23f3-107">PR_PROVIDER_SUBMIT_TIME</span></span>  <br/> |
|<span data-ttu-id="b23f3-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="b23f3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b23f3-109">0x0048</span><span class="sxs-lookup"><span data-stu-id="b23f3-109">0x0048</span></span>  <br/> |
|<span data-ttu-id="b23f3-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="b23f3-110">Data type:</span></span>  <br/> |<span data-ttu-id="b23f3-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="b23f3-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="b23f3-112">Área:</span><span class="sxs-lookup"><span data-stu-id="b23f3-112">Area:</span></span>  <br/> |<span data-ttu-id="b23f3-113">Envelope MAPI</span><span class="sxs-lookup"><span data-stu-id="b23f3-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b23f3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b23f3-114">Remarks</span></span>

<span data-ttu-id="b23f3-115">Essa propriedade é definida pelo provedor de transporte de saída no momento em que uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="b23f3-115">This property is set by the outgoing transport provider at the time a message is sent.</span></span>
  
<span data-ttu-id="b23f3-116">Essa propriedade corresponde a um atributo por mensagem de envelope de envio de x. 400.</span><span class="sxs-lookup"><span data-stu-id="b23f3-116">This property corresponds to an X.400 submission envelope per-message attribute.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="b23f3-117">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="b23f3-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="b23f3-118">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b23f3-118">Header files</span></span>

<span data-ttu-id="b23f3-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b23f3-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="b23f3-120">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="b23f3-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="b23f3-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="b23f3-121">Mapitags.h</span></span>
  
> <span data-ttu-id="b23f3-122">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="b23f3-122">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b23f3-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="b23f3-123">See also</span></span>



[<span data-ttu-id="b23f3-124">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="b23f3-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b23f3-125">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="b23f3-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b23f3-126">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="b23f3-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b23f3-127">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="b23f3-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

