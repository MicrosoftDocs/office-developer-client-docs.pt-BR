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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422240"
---
# <a name="pidtagabproviderid-canonical-property"></a><span data-ttu-id="dbedc-103">Propriedade canônica PidTagAbProviderId</span><span class="sxs-lookup"><span data-stu-id="dbedc-103">PidTagAbProviderId Canonical Property</span></span>

  
  
<span data-ttu-id="dbedc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dbedc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dbedc-105">Contém uma estrutura [MAPIUID](mapiuid.md) do provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dbedc-105">Contains an address book provider's [MAPIUID](mapiuid.md) structure.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dbedc-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="dbedc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="dbedc-107">PR_AB_PROVIDER_ID</span><span class="sxs-lookup"><span data-stu-id="dbedc-107">PR_AB_PROVIDER_ID</span></span>  <br/> |
|<span data-ttu-id="dbedc-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="dbedc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="dbedc-109">0x3615</span><span class="sxs-lookup"><span data-stu-id="dbedc-109">0x3615</span></span>  <br/> |
|<span data-ttu-id="dbedc-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="dbedc-110">Data type:</span></span>  <br/> |<span data-ttu-id="dbedc-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="dbedc-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="dbedc-112">Área:</span><span class="sxs-lookup"><span data-stu-id="dbedc-112">Area:</span></span>  <br/> |<span data-ttu-id="dbedc-113">Catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="dbedc-113">Address book</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbedc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbedc-114">Remarks</span></span>

<span data-ttu-id="dbedc-115">A estrutura **MAPIUID** identifica qual provedor de catálogo de endereços fornece esse contêiner específico na hierarquia do contêiner.</span><span class="sxs-lookup"><span data-stu-id="dbedc-115">The **MAPIUID** structure identifies which address book provider supplies this particular container in the container hierarchy.</span></span> <span data-ttu-id="dbedc-116">O valor é exclusivo para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="dbedc-116">The value is unique to each provider.</span></span> 
  
<span data-ttu-id="dbedc-117">Um provedor de catálogo de endereços pode fornecer mais de um identificador.</span><span class="sxs-lookup"><span data-stu-id="dbedc-117">An address book provider can provide more than one identifier.</span></span> <span data-ttu-id="dbedc-118">Por exemplo, um provedor que forneça dois contêineres diferentes pode publicar em **PR_AB_PROVIDER_ID** identificadores exclusivos para cada contêiner.</span><span class="sxs-lookup"><span data-stu-id="dbedc-118">For example, a provider that supplies two different containers can publish in **PR_AB_PROVIDER_ID** unique identifiers for each container.</span></span> 
  
 <span data-ttu-id="dbedc-119">**PR_AB_PROVIDER_ID** é análogo à propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para repositórios de mensagens.</span><span class="sxs-lookup"><span data-stu-id="dbedc-119">**PR_AB_PROVIDER_ID** is analogous to the **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) property for message stores.</span></span> <span data-ttu-id="dbedc-120">Os aplicativos cliente podem usar o **PR_AB_PROVIDER_ID** para localizar linhas relacionadas em uma tabela de hierarquia de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="dbedc-120">Client applications can use **PR_AB_PROVIDER_ID** to find related rows in an address book hierarchy table.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="dbedc-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbedc-121">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="dbedc-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dbedc-122">Header files</span></span>

<span data-ttu-id="dbedc-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="dbedc-123">Mapitags.h</span></span>
  
> <span data-ttu-id="dbedc-124">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="dbedc-124">Contains definitions of properties listed as associated properties.</span></span>
    
<span data-ttu-id="dbedc-125">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="dbedc-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="dbedc-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="dbedc-126">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="dbedc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbedc-127">See also</span></span>



[<span data-ttu-id="dbedc-128">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="dbedc-128">MAPIUID</span></span>](mapiuid.md)
  
[<span data-ttu-id="dbedc-129">Propriedade canônica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="dbedc-129">PidTagStoreProvider Canonical Property</span></span>](pidtagstoreprovider-canonical-property.md)


[<span data-ttu-id="dbedc-130">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="dbedc-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="dbedc-131">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="dbedc-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="dbedc-132">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="dbedc-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

