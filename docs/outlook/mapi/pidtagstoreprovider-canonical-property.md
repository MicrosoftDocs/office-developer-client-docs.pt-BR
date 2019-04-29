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
ms.openlocfilehash: 6266c9293f54ce764c5b5b0e41d43767490abcf7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412048"
---
# <a name="pidtagstoreprovider-canonical-property"></a><span data-ttu-id="fba87-103">Propriedade canônica PidTagStoreProvider</span><span class="sxs-lookup"><span data-stu-id="fba87-103">PidTagStoreProvider Canonical Property</span></span>

  
  
<span data-ttu-id="fba87-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fba87-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fba87-105">Contém uma estrutura [MAPIUID](mapiuid.md) definida pelo provedor que indica o tipo do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fba87-105">Contains a provider-defined [MAPIUID](mapiuid.md) structure that indicates the type of the message store.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fba87-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fba87-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fba87-107">PR_MDB_PROVIDER</span><span class="sxs-lookup"><span data-stu-id="fba87-107">PR_MDB_PROVIDER</span></span>  <br/> |
|<span data-ttu-id="fba87-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fba87-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fba87-109">0x3414</span><span class="sxs-lookup"><span data-stu-id="fba87-109">0x3414</span></span>  <br/> |
|<span data-ttu-id="fba87-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fba87-110">Data type:</span></span>  <br/> |<span data-ttu-id="fba87-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="fba87-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="fba87-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fba87-112">Area:</span></span>  <br/> |<span data-ttu-id="fba87-113">Propriedades de ID</span><span class="sxs-lookup"><span data-stu-id="fba87-113">ID properties</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fba87-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fba87-114">Remarks</span></span>

<span data-ttu-id="fba87-115">A estrutura [MAPIUID](mapiuid.md) identifica o tipo de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="fba87-115">The [MAPIUID](mapiuid.md) structure identifies the type of message store.</span></span> <span data-ttu-id="fba87-116">O valor é calculado por provedores de repositórios de mensagens em objetos do repositório de mensagens e é exclusivo para cada provedor.</span><span class="sxs-lookup"><span data-stu-id="fba87-116">The value is computed by message store providers on message store objects and is unique to each provider.</span></span> <span data-ttu-id="fba87-117">Normalmente, é usado para navegar pela tabela de repositórios de mensagens para localizar um repositório do tipo desejado, como pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="fba87-117">It is typically used for browsing through the message store table to find a store of the desired type, such as public folders.</span></span> 
  
<span data-ttu-id="fba87-118">Essa propriedade é análoga à propriedade **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) para catálogos de endereços.</span><span class="sxs-lookup"><span data-stu-id="fba87-118">This property is analogous to the **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) property for address books.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fba87-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fba87-119">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="fba87-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fba87-120">Header files</span></span>

<span data-ttu-id="fba87-121">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="fba87-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fba87-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fba87-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fba87-123">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="fba87-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fba87-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fba87-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fba87-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fba87-125">See also</span></span>



[<span data-ttu-id="fba87-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fba87-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fba87-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="fba87-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fba87-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fba87-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fba87-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fba87-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

