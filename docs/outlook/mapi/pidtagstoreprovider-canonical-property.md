---
title: Propriedade canônica PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b634f815d2aedecc716227c6525b846db38ca869
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770085"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="d0e5d-103">Propriedade canônica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="d0e5d-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="d0e5d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d0e5d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d0e5d-105">Contém uma estrutura [MAPIUID](mapiuid.md) definido pelo provedor que indica o tipo de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0e5d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d0e5d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0e5d-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="d0e5d-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="d0e5d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0e5d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0e5d-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="d0e5d-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="d0e5d-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d0e5d-110">Data type:</span></span>  <br/> |<span data-ttu-id="d0e5d-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d0e5d-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d0e5d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d0e5d-112">Area:</span></span>  <br/> |<span data-ttu-id="d0e5d-113">Propriedades de identificação</span><span class="sxs-lookup"><span data-stu-id="d0e5d-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0e5d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d0e5d-114">Remarks</span></span>

<span data-ttu-id="d0e5d-115">A estrutura [MAPIUID](mapiuid.md) identifica o tipo de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="d0e5d-116">O valor é computado pelo provedores de armazenamento de mensagem em objetos de repositório de mensagem e é exclusivo para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="d0e5d-117">Normalmente, ele é usado para pesquisar pela tabela de repositório de mensagens para localizar um repositório do tipo desejado, como pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="d0e5d-118">Essa propriedade é semelhante à propriedade **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) para catálogos de endereços.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d0e5d-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0e5d-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d0e5d-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d0e5d-120">Header files</span></span>

<span data-ttu-id="d0e5d-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0e5d-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0e5d-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0e5d-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0e5d-123">Mapitags.h</span></span>
  
> <span data-ttu-id="d0e5d-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d0e5d-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0e5d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0e5d-125">See also</span></span>



[<span data-ttu-id="d0e5d-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d0e5d-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0e5d-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d0e5d-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0e5d-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d0e5d-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0e5d-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d0e5d-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

