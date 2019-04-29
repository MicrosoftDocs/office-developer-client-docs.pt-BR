---
title: Propriedade canônica PidTagIdentityDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIdentityDisplay
api_type:
- HeaderDef
ms.assetid: ad9756c1-c1f9-4ab3-a58a-31e574dd9530
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d6e189f78dec2fc92f1804be93e7885b61734b03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431418"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="0eb4d-103">Propriedade canônica PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="0eb4d-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="0eb4d-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eb4d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eb4d-105">Contém o nome de exibição da identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0eb4d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0eb4d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0eb4d-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="0eb4d-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="0eb4d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0eb4d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0eb4d-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="0eb4d-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="0eb4d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0eb4d-110">Data type:</span></span>  <br/> |<span data-ttu-id="0eb4d-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0eb4d-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="0eb4d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0eb4d-112">Area:</span></span>  <br/> |<span data-ttu-id="0eb4d-113">Status de MAPI</span><span class="sxs-lookup"><span data-stu-id="0eb4d-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0eb4d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0eb4d-114">Remarks</span></span>

<span data-ttu-id="0eb4d-115">Essas propriedades não aparecem como propriedades em qualquer objeto, mas somente como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="0eb4d-116">Ele faz parte da identidade do provedor de serviços que expõe a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="0eb4d-117">A identidade do provedor geralmente se refere à sua conta no servidor, mas pode se referir a qualquer representação que o provedor define no sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="0eb4d-118">Um provedor de serviços que forneça qualquer uma das propriedades de identidade deve fornecer todos eles.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="0eb4d-119">Os provedores que pertencem ao mesmo serviço de mensagens devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0eb4d-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0eb4d-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0eb4d-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0eb4d-121">Header files</span></span>

<span data-ttu-id="0eb4d-122">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="0eb4d-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="0eb4d-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="0eb4d-124">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="0eb4d-124">Mapitags.h</span></span>
  
> <span data-ttu-id="0eb4d-125">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="0eb4d-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0eb4d-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0eb4d-126">See also</span></span>



[<span data-ttu-id="0eb4d-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="0eb4d-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="0eb4d-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="0eb4d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0eb4d-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="0eb4d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0eb4d-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0eb4d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0eb4d-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0eb4d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

