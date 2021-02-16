---
title: Propriedade canônica PidTagStatusCode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusCode
api_type:
- COM
ms.assetid: e29190c5-52c3-4ef7-98db-699487c54325
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 751be8abe02dfb1d5bab2bcbbbc0cbd2a8243f85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418511"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="34eeb-103">Propriedade canônica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="34eeb-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="34eeb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34eeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34eeb-105">Contém uma máscara de bits de sinalizadores que indicam o status atual de um recurso de sessão.</span><span class="sxs-lookup"><span data-stu-id="34eeb-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="34eeb-106">Todos os provedores de serviços configuram códigos de status, assim como o MAPI para relatar o status do subsistema, o spooler MAPI e o livro de endereços integrado.</span><span class="sxs-lookup"><span data-stu-id="34eeb-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="34eeb-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="34eeb-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="34eeb-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="34eeb-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="34eeb-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="34eeb-109">Identifier:</span></span>  <br/> |<span data-ttu-id="34eeb-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="34eeb-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="34eeb-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="34eeb-111">Data type:</span></span>  <br/> |<span data-ttu-id="34eeb-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="34eeb-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="34eeb-113">Área:</span><span class="sxs-lookup"><span data-stu-id="34eeb-113">Area:</span></span>  <br/> |<span data-ttu-id="34eeb-114">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="34eeb-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="34eeb-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="34eeb-115">Remarks</span></span>

<span data-ttu-id="34eeb-116">O código de status deve aparecer no arquivo Mapisvc.inf para todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="34eeb-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="34eeb-117">Os objetos de status são implementados por MAPI e por todos os provedores de serviços.</span><span class="sxs-lookup"><span data-stu-id="34eeb-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="34eeb-118">Há dois conjuntos de valores válidos para códigos de status, um conjunto para todos os objetos de status e outro conjunto apenas para provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="34eeb-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="34eeb-119">Todos os objetos de status podem definir essa propriedade com os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="34eeb-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="34eeb-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="34eeb-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="34eeb-121">Indica que o recurso está operacional.</span><span class="sxs-lookup"><span data-stu-id="34eeb-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="34eeb-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="34eeb-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="34eeb-123">Indica que o recurso está enfrentando um problema.</span><span class="sxs-lookup"><span data-stu-id="34eeb-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="34eeb-124">Para provedores de serviços, STATUS_FAILURE indica que o provedor poderá ser desligado em breve para encerrar a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="34eeb-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="34eeb-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="34eeb-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="34eeb-126">Indica que somente os dados ou serviços locais estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="34eeb-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="34eeb-127">Os provedores de transporte também podem definir as propriedades de PR_STATUS_CODE **status** para os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="34eeb-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="34eeb-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="34eeb-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="34eeb-129">Indica que o provedor de transporte está recebendo uma mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="34eeb-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="34eeb-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="34eeb-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="34eeb-131">Indica que o provedor de transporte pode receber mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="34eeb-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="34eeb-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="34eeb-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="34eeb-133">Indica que o provedor de transporte está baixando mensagens da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="34eeb-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="34eeb-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="34eeb-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="34eeb-135">Indica que o provedor de transporte está recebendo uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="34eeb-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="34eeb-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="34eeb-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="34eeb-137">Indica que o provedor de transporte pode lidar com mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="34eeb-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="34eeb-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="34eeb-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="34eeb-139">Indica que o provedor de transporte está carregando mensagens da fila de saída.</span><span class="sxs-lookup"><span data-stu-id="34eeb-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="34eeb-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="34eeb-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="34eeb-141">Indica que o provedor de transporte oferece suporte ao acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="34eeb-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="34eeb-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="34eeb-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="34eeb-143">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="34eeb-143">Header files</span></span>

<span data-ttu-id="34eeb-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="34eeb-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="34eeb-145">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="34eeb-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="34eeb-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="34eeb-146">Mapitags.h</span></span>
  
> <span data-ttu-id="34eeb-147">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="34eeb-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="34eeb-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="34eeb-148">See also</span></span>



[<span data-ttu-id="34eeb-149">Propriedade canônica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="34eeb-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="34eeb-150">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="34eeb-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="34eeb-151">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="34eeb-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="34eeb-152">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="34eeb-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="34eeb-153">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="34eeb-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

