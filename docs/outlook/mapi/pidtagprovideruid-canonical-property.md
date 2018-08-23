---
title: Propriedade canônica PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cca22b466b1e0d2da9ca9cc009586df08316270c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581052"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="3bfc9-103">Propriedade canônica PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="3bfc9-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="3bfc9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bfc9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bfc9-105">Contém uma estrutura **MAPIUID** do provedor de serviços que está tratando a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bfc9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="3bfc9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="3bfc9-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="3bfc9-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="3bfc9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="3bfc9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="3bfc9-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="3bfc9-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="3bfc9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="3bfc9-110">Data type:</span></span>  <br/> |<span data-ttu-id="3bfc9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="3bfc9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="3bfc9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="3bfc9-112">Area:</span></span>  <br/> |<span data-ttu-id="3bfc9-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="3bfc9-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bfc9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bfc9-114">Remarks</span></span>

<span data-ttu-id="3bfc9-115">Essa propriedade é computada pelo todos os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-115">This property is computed by all service providers.</span></span> <span data-ttu-id="3bfc9-116">Ele contém uma estrutura [MAPIUID](mapiuid.md) associada e geralmente codificadas, pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="3bfc9-117">Normalmente, ele é usado por um aplicativo cliente que está interessado em somente os contêineres de catálogo de endereços fornecidos por um provedor específico.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="3bfc9-118">Essa propriedade será exibida apenas como uma entrada de coluna da tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="3bfc9-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="3bfc9-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="3bfc9-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3bfc9-120">Header files</span></span>

<span data-ttu-id="3bfc9-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bfc9-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="3bfc9-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="3bfc9-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="3bfc9-123">Mapitags.h</span></span>
  
> <span data-ttu-id="3bfc9-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="3bfc9-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3bfc9-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bfc9-125">See also</span></span>



[<span data-ttu-id="3bfc9-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfc9-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="3bfc9-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="3bfc9-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="3bfc9-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="3bfc9-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="3bfc9-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="3bfc9-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

