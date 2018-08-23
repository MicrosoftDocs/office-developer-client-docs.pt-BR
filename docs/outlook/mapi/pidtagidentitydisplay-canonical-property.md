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
ms.openlocfilehash: 6cfc4d6eab5b2f19bcfd4c7e2a8fc9fa1494afa4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585574"
---
# <a name="pidtagidentitydisplay-canonical-property"></a><span data-ttu-id="c9b4b-103">Propriedade canônica PidTagIdentityDisplay</span><span class="sxs-lookup"><span data-stu-id="c9b4b-103">PidTagIdentityDisplay Canonical Property</span></span>

  
  
<span data-ttu-id="c9b4b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c9b4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c9b4b-105">Contém o nome de exibição para a identidade de um provedor de serviços, conforme definido em um sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-105">Contains the display name for a service provider's identity as defined within a messaging system.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9b4b-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c9b4b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c9b4b-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span><span class="sxs-lookup"><span data-stu-id="c9b4b-107">PR_IDENTITY_DISPLAY, PR_IDENTITY_DISPLAY_A, PR_IDENTITY_DISPLAY_W</span></span>  <br/> |
|<span data-ttu-id="c9b4b-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c9b4b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c9b4b-109">0x3E00</span><span class="sxs-lookup"><span data-stu-id="c9b4b-109">0x3E00</span></span>  <br/> |
|<span data-ttu-id="c9b4b-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c9b4b-110">Data type:</span></span>  <br/> |<span data-ttu-id="c9b4b-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="c9b4b-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="c9b4b-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c9b4b-112">Area:</span></span>  <br/> |<span data-ttu-id="c9b4b-113">Status MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b4b-113">MAPI status</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9b4b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9b4b-114">Remarks</span></span>

<span data-ttu-id="c9b4b-115">Essas propriedades não aparecem como propriedades em qualquer objeto, mas apenas como uma coluna em uma tabela de status.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-115">These properties do not appear as properties on any object but only as a column in a status table.</span></span> <span data-ttu-id="c9b4b-116">Ele é parte da identidade do provedor de serviços expondo a linha da tabela de status.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-116">It is part of the identity of the service provider exposing the status table row.</span></span> <span data-ttu-id="c9b4b-117">Normalmente, a identidade do provedor refere-se a sua conta no servidor, mas pode se referir a qualquer representação que o provedor define dentro do sistema de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-117">The provider's identity typically refers to its account on the server, but can refer to any representation the provider defines within the messaging system.</span></span> 
  
<span data-ttu-id="c9b4b-118">Um provedor de serviços que forneçam qualquer uma das propriedades identity deve fornecer aos todos eles.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-118">A service provider furnishing any of the identity properties should furnish all of them.</span></span> <span data-ttu-id="c9b4b-119">Os provedores que pertencem ao mesmo serviço de mensagem devem expor os mesmos valores para as propriedades de identidade.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-119">Providers that belong to the same message service should expose the same values for the identity properties.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c9b4b-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9b4b-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="c9b4b-121">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9b4b-121">Header files</span></span>

<span data-ttu-id="c9b4b-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c9b4b-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="c9b4b-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="c9b4b-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="c9b4b-124">Mapitags.h</span></span>
  
> <span data-ttu-id="c9b4b-125">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c9b4b-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c9b4b-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9b4b-126">See also</span></span>



[<span data-ttu-id="c9b4b-127">IMAPISession::QueryIdentity</span><span class="sxs-lookup"><span data-stu-id="c9b4b-127">IMAPISession::QueryIdentity</span></span>](imapisession-queryidentity.md)


[<span data-ttu-id="c9b4b-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b4b-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c9b4b-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="c9b4b-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c9b4b-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c9b4b-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c9b4b-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c9b4b-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

