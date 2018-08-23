---
title: Propriedade canônica PidTagStatusString
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatusString
api_type:
- COM
ms.assetid: 42cd946c-c55a-4371-99ee-05e2248fdd5f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e8370a613162e3bc8d4395a18e9a7e177255b9b3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567297"
---
# <a name="pidtagstatusstring-canonical-property"></a><span data-ttu-id="3f49e-103">Propriedade canônica PidTagStatusString</span><span class="sxs-lookup"><span data-stu-id="3f49e-103">PidTagStatusString Canonical Property</span></span>

  
  
<span data-ttu-id="3f49e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3f49e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3f49e-105">Contém uma mensagem que indica o status atual de um recurso de sessão.</span><span class="sxs-lookup"><span data-stu-id="3f49e-105">Contains a message that indicates the current status of a session resource.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f49e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3f49e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3f49e-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span><span class="sxs-lookup"><span data-stu-id="3f49e-107">PR_STATUS_STRING, PR_STATUS_STRING_A, PR_STATUS_STRING_W</span></span>  <br/> |
|<span data-ttu-id="3f49e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3f49e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3f49e-109">0x3E08</span><span class="sxs-lookup"><span data-stu-id="3f49e-109">0x3E08</span></span>  <br/> |
|<span data-ttu-id="3f49e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3f49e-110">Data type:</span></span>  <br/> |<span data-ttu-id="3f49e-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3f49e-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="3f49e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3f49e-112">Area:</span></span>  <br/> |<span data-ttu-id="3f49e-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="3f49e-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3f49e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f49e-114">Remarks</span></span>

<span data-ttu-id="3f49e-115">Essas propriedades dê provedores de serviços e a oportunidade de fornecer informações específicas sobre o status de um recurso de sessão, como o catálogo de endereços integrada ou um provedor de serviço específico de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3f49e-115">These properties give service providers and MAPI the opportunity to supply specific information about the status of a session resource, such as the integrated address book or a particular service provider.</span></span> <span data-ttu-id="3f49e-116">Essa propriedade explica e fornece informações adicionais sobre um código de status ou a propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3f49e-116">This property explains and provides additional information about a status code, or the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property.</span></span> <span data-ttu-id="3f49e-117">Enquanto **PR_STATUS_CODE** é necessário para todos os objetos de status, **PR_STATUS_STRING** e propriedades associadas são opcionais.</span><span class="sxs-lookup"><span data-stu-id="3f49e-117">Whereas **PR_STATUS_CODE** is required for all status objects, **PR_STATUS_STRING** and associated properties are optional.</span></span> <span data-ttu-id="3f49e-118">Quando o provedor de transporte não fornecer um valor, o MAPI spooler fornece um valor padrão.</span><span class="sxs-lookup"><span data-stu-id="3f49e-118">When the transport provider does not supply a value, the MAPI spooler supplies a default value.</span></span> 
  
<span data-ttu-id="3f49e-119">A cadeia de caracteres é gerada no mesmo lado da chamada de procedimento remoto como o spooler MAPI; ela se movimenta por meio de memória compartilhada em vez de ser empacotados em um limite de processo.</span><span class="sxs-lookup"><span data-stu-id="3f49e-119">The string is generated on the same side of the remote procedure call as the MAPI spooler; it travels through shared memory rather than being marshaled across a process boundary.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3f49e-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3f49e-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3f49e-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3f49e-121">Header files</span></span>

<span data-ttu-id="3f49e-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3f49e-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="3f49e-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3f49e-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="3f49e-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3f49e-124">Mapitags.h</span></span>
  
> <span data-ttu-id="3f49e-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3f49e-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3f49e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f49e-126">See also</span></span>



[<span data-ttu-id="3f49e-127">Propriedade canônica PidTagStatusCode</span><span class="sxs-lookup"><span data-stu-id="3f49e-127">PidTagStatusCode Canonical Property</span></span>](pidtagstatuscode-canonical-property.md)


[<span data-ttu-id="3f49e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3f49e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3f49e-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3f49e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3f49e-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3f49e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3f49e-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3f49e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

