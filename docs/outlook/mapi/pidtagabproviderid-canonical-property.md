---
title: Propriedade canônica PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f3aad4a5b3ba815d3e4f91e990bb63d75502f94b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580072"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="0f256-103">Propriedade canônica PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="0f256-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="0f256-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0f256-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0f256-105">Contém a estrutura [MAPIUID](mapiuid.md) de um provedor catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="0f256-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0f256-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="0f256-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0f256-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="0f256-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="0f256-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="0f256-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0f256-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="0f256-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="0f256-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="0f256-110">Data type:</span></span>  <br/> |<span data-ttu-id="0f256-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0f256-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0f256-112">Área:</span><span class="sxs-lookup"><span data-stu-id="0f256-112">Area:</span></span>  <br/> |<span data-ttu-id="0f256-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="0f256-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f256-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f256-114">Remarks</span></span>

<span data-ttu-id="0f256-115">A estrutura **MAPIUID** identifica qual provedor de catálogo de endereços fornece nesse contêiner específico na hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="0f256-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="0f256-116">O valor é exclusivo para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="0f256-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="0f256-117">Um provedor de catálogo de endereços pode fornecer mais de um identificador.</span><span class="sxs-lookup"><span data-stu-id="0f256-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="0f256-118">Por exemplo, um provedor que fornece dois contêineres diferentes pode publicar em **PR_AB_PROVIDER_ID** de identificadores exclusivos para cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="0f256-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="0f256-119">**PR_AB_PROVIDER_ID** é semelhante à propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para repositórios de mensagem.</span><span class="sxs-lookup"><span data-stu-id="0f256-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="0f256-120">Aplicativos cliente podem usar **PR_AB_PROVIDER_ID** para localizar linhas relacionadas em uma tabela de hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="0f256-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0f256-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f256-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0f256-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f256-122">Header files</span></span>

<span data-ttu-id="0f256-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0f256-123">Mapitags.h</span></span>
  
> <span data-ttu-id="0f256-124">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="0f256-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="0f256-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0f256-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="0f256-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="0f256-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0f256-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f256-127">See also</span></span>



[<span data-ttu-id="0f256-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="0f256-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="0f256-129">Propriedade canônica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="0f256-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="0f256-130">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="0f256-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0f256-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="0f256-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0f256-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="0f256-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

