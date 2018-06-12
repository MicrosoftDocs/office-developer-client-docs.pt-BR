---
title: Propriedade canônico de PidTagProviderUid
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769704"
---
# <a name="pidtagprovideruid-canonical-property"></a><span data-ttu-id="e7339-103">Propriedade canônico de PidTagProviderUid</span><span class="sxs-lookup"><span data-stu-id="e7339-103">PidTagProviderUid Canonical Property</span></span>

  
  
<span data-ttu-id="e7339-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e7339-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e7339-105">Contém uma estrutura **MAPIUID** do provedor de serviços que está tratando a uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7339-105">Contains a **MAPIUID** structure of the service provider that is handling a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e7339-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e7339-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7339-107">PR_PROVIDER_UID</span><span class="sxs-lookup"><span data-stu-id="e7339-107">PR_PROVIDER_UID</span></span>  <br/> |
|<span data-ttu-id="e7339-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e7339-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e7339-109">0x300C</span><span class="sxs-lookup"><span data-stu-id="e7339-109">0x300C</span></span>  <br/> |
|<span data-ttu-id="e7339-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e7339-110">Data type:</span></span>  <br/> |<span data-ttu-id="e7339-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="e7339-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="e7339-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e7339-112">Area:</span></span>  <br/> |<span data-ttu-id="e7339-113">MAPI comuns</span><span class="sxs-lookup"><span data-stu-id="e7339-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7339-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e7339-114">Remarks</span></span>

<span data-ttu-id="e7339-115">Essa propriedade é computada pelo todos os provedores de serviço.</span><span class="sxs-lookup"><span data-stu-id="e7339-115">This property is computed by all service providers.</span></span> <span data-ttu-id="e7339-116">Ele contém uma estrutura [MAPIUID](mapiuid.md) associada e geralmente codificadas, pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="e7339-116">It contains a [MAPIUID](mapiuid.md) structure associated with, and usually hard-coded by, the provider.</span></span> <span data-ttu-id="e7339-117">Normalmente, ele é usado por um aplicativo cliente que está interessado em somente os contêineres de catálogo de endereços fornecidos por um provedor específico.</span><span class="sxs-lookup"><span data-stu-id="e7339-117">It is typically used by a client application that is interested in only the address book containers supplied by a particular provider.</span></span> 
  
<span data-ttu-id="e7339-118">Essa propriedade será exibida apenas como uma entrada de coluna da tabela de provedor.</span><span class="sxs-lookup"><span data-stu-id="e7339-118">This property appears only as a column entry in the provider table.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7339-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7339-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e7339-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7339-120">Header files</span></span>

<span data-ttu-id="e7339-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e7339-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7339-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e7339-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="e7339-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e7339-123">Mapitags.h</span></span>
  
> <span data-ttu-id="e7339-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e7339-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7339-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7339-125">See also</span></span>



[<span data-ttu-id="e7339-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e7339-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7339-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e7339-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7339-128">Mapear nomes de propriedade canônico para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e7339-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7339-129">Mapear nomes de MAPI para nomes de propriedade canônico</span><span class="sxs-lookup"><span data-stu-id="e7339-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

