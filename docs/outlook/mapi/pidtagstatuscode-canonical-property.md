---
title: Propriedade canônico de PidTagStatusCode
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: efd0dcc8fc01fa433cbbf30936244e4818f8b14a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770076"
---
# <a name="pidtagstatuscode-canonical-property"></a><span data-ttu-id="61cd3-103">Propriedade canônico de PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="61cd3-103">PidTagStatusCode Canonical Property</span></span>

  
  
<span data-ttu-id="61cd3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="61cd3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="61cd3-105">Contém uma bitmask dos sinalizadores que indicam o status atual de um recurso de sessão.</span><span class="sxs-lookup"><span data-stu-id="61cd3-105">Contains a bitmask of flags that indicate the current status of a session resource.</span></span> <span data-ttu-id="61cd3-106">Todos os provedores de serviço definir códigos de status como MAPI a ser relatado no status do catálogo de endereços integrada, o MAPI spooler e o subsistema de faz.</span><span class="sxs-lookup"><span data-stu-id="61cd3-106">All service providers set status codes as does MAPI to report on the status of the subsystem, the MAPI spooler, and the integrated address book.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61cd3-107">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="61cd3-107">Associated properties:</span></span>  <br/> |<span data-ttu-id="61cd3-108">PR_STATUS_CODE</span><span class="sxs-lookup"><span data-stu-id="61cd3-108">PR_STATUS_CODE</span></span>  <br/> |
|<span data-ttu-id="61cd3-109">Identificador:</span><span class="sxs-lookup"><span data-stu-id="61cd3-109">Identifier:</span></span>  <br/> |<span data-ttu-id="61cd3-110">0x3E04</span><span class="sxs-lookup"><span data-stu-id="61cd3-110">0x3E04</span></span>  <br/> |
|<span data-ttu-id="61cd3-111">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="61cd3-111">Data type:</span></span>  <br/> |<span data-ttu-id="61cd3-112">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="61cd3-112">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="61cd3-113">Área:</span><span class="sxs-lookup"><span data-stu-id="61cd3-113">Area:</span></span>  <br/> |<span data-ttu-id="61cd3-114">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="61cd3-114">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61cd3-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="61cd3-115">Remarks</span></span>

<span data-ttu-id="61cd3-116">O código de status deve aparecer no arquivo Mapisvc para todos os provedores.</span><span class="sxs-lookup"><span data-stu-id="61cd3-116">The status code must appear in the Mapisvc.inf file for all providers.</span></span> 
  
<span data-ttu-id="61cd3-117">Objetos de status são implementados por MAPI e por todos os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="61cd3-117">Status objects are implemented by MAPI and by all service providers.</span></span> <span data-ttu-id="61cd3-118">Há dois conjuntos de valores válidos para códigos de status, um conjunto de todos os objetos de status e outro conjunto para apenas os provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="61cd3-118">There are two sets of valid values for status codes, one set for all status objects and another set for transport providers only.</span></span> <span data-ttu-id="61cd3-119">Todos os objetos de status podem definir essa propriedade para os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="61cd3-119">All status objects can set this property to the following values:</span></span>
  
<span data-ttu-id="61cd3-120">STATUS_AVAILABLE</span><span class="sxs-lookup"><span data-stu-id="61cd3-120">STATUS_AVAILABLE</span></span> 
  
> <span data-ttu-id="61cd3-121">Indica se o recurso está em operação.</span><span class="sxs-lookup"><span data-stu-id="61cd3-121">Indicates that the resource is operational.</span></span>
    
<span data-ttu-id="61cd3-122">STATUS_FAILURE</span><span class="sxs-lookup"><span data-stu-id="61cd3-122">STATUS_FAILURE</span></span> 
  
> <span data-ttu-id="61cd3-123">Indica que o recurso está com problemas.</span><span class="sxs-lookup"><span data-stu-id="61cd3-123">Indicates that the resource is experiencing a problem.</span></span> <span data-ttu-id="61cd3-124">Para provedores de serviço, STATUS_FAILURE indica que o provedor talvez breve sejam desligado para terminar a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="61cd3-124">For service providers, STATUS_FAILURE indicates that the provider might soon be shut down to end the current session.</span></span>
    
<span data-ttu-id="61cd3-125">STATUS_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="61cd3-125">STATUS_OFFLINE</span></span> 
  
> <span data-ttu-id="61cd3-126">Indica que os dados apenas locais ou serviços estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="61cd3-126">Indicates that only local data or services are available.</span></span>
    
<span data-ttu-id="61cd3-127">Provedores de transporte também podem definir seu status **PR_STATUS_CODE** propriedades dos objetos para os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="61cd3-127">Transport providers can also set their status objects' **PR_STATUS_CODE** properties to the following values:</span></span> 
  
<span data-ttu-id="61cd3-128">STATUS_INBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="61cd3-128">STATUS_INBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="61cd3-129">Indica que o provedor de transporte está recebendo uma mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="61cd3-129">Indicates that the transport provider is receiving an inbound message.</span></span> 
    
<span data-ttu-id="61cd3-130">STATUS_INBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="61cd3-130">STATUS_INBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="61cd3-131">Indica que o provedor de transporte pode receber mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="61cd3-131">Indicates that the transport provider can receive inbound messages.</span></span>
    
<span data-ttu-id="61cd3-132">STATUS_INBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="61cd3-132">STATUS_INBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="61cd3-133">Indica que o provedor de transporte é baixando mensagens da fila de entrada.</span><span class="sxs-lookup"><span data-stu-id="61cd3-133">Indicates that the transport provider is downloading messages from the inbound queue.</span></span>
    
<span data-ttu-id="61cd3-134">STATUS_OUTBOUND_ACTIVE</span><span class="sxs-lookup"><span data-stu-id="61cd3-134">STATUS_OUTBOUND_ACTIVE</span></span> 
  
> <span data-ttu-id="61cd3-135">Indica que o provedor de transporte está recebendo uma mensagem de saída.</span><span class="sxs-lookup"><span data-stu-id="61cd3-135">Indicates that the transport provider is receiving an outbound message.</span></span> 
    
<span data-ttu-id="61cd3-136">STATUS_OUTBOUND_ENABLED</span><span class="sxs-lookup"><span data-stu-id="61cd3-136">STATUS_OUTBOUND_ENABLED</span></span> 
  
> <span data-ttu-id="61cd3-137">Indica que o provedor de transporte pode manipular mensagens de saída.</span><span class="sxs-lookup"><span data-stu-id="61cd3-137">Indicates that the transport provider can handle outbound messages.</span></span>
    
<span data-ttu-id="61cd3-138">STATUS_OUTBOUND_FLUSH</span><span class="sxs-lookup"><span data-stu-id="61cd3-138">STATUS_OUTBOUND_FLUSH</span></span> 
  
> <span data-ttu-id="61cd3-139">Indica que o provedor de transporte está carregando mensagens de sua fila de saída.</span><span class="sxs-lookup"><span data-stu-id="61cd3-139">Indicates that the transport provider is uploading messages from its outbound queue.</span></span>
    
<span data-ttu-id="61cd3-140">STATUS_REMOTE_ACCESS</span><span class="sxs-lookup"><span data-stu-id="61cd3-140">STATUS_REMOTE_ACCESS</span></span> 
  
> <span data-ttu-id="61cd3-141">Indica que o provedor de transporte suporta acesso remoto.</span><span class="sxs-lookup"><span data-stu-id="61cd3-141">Indicates that the transport provider supports remote access.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="61cd3-142">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="61cd3-142">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="61cd3-143">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61cd3-143">Header files</span></span>

<span data-ttu-id="61cd3-144">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="61cd3-144">Mapidefs.h</span></span>
  
> <span data-ttu-id="61cd3-145">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="61cd3-145">Provides data type definitions.</span></span>
    
<span data-ttu-id="61cd3-146">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="61cd3-146">Mapitags.h</span></span>
  
> <span data-ttu-id="61cd3-147">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="61cd3-147">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="61cd3-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="61cd3-148">See also</span></span>



[<span data-ttu-id="61cd3-149">Propriedade canônico de PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="61cd3-149">PidTagStatusString Canonical Property</span></span>](pidtagstatusstring-canonical-property.md)


[<span data-ttu-id="61cd3-150">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="61cd3-150">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="61cd3-151">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="61cd3-151">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="61cd3-152">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="61cd3-152">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="61cd3-153">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="61cd3-153">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

