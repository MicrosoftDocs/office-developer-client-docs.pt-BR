---
title: Propriedade canônica PidTagAutoForwarded
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAutoForwarded
api_type:
- HeaderDef
ms.assetid: 1ba40cc2-ba27-4d75-9682-c536cf3a0d58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8303a60ee0d61a56c79fadf471bc6111fcbde7d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769002"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="e9e0f-103">Propriedade canônica PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="e9e0f-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="e9e0f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e9e0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e9e0f-105">Conterá TRUE se o cliente solicita um campo de cabeçalho X-MS-Exchange-organização-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9e0f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e9e0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9e0f-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="e9e0f-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="e9e0f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e9e0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9e0f-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="e9e0f-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="e9e0f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e9e0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9e0f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e9e0f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e9e0f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e9e0f-112">Area:</span></span>  <br/> |<span data-ttu-id="e9e0f-113">Relatório geral</span><span class="sxs-lookup"><span data-stu-id="e9e0f-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9e0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9e0f-114">Remarks</span></span>

<span data-ttu-id="e9e0f-115">Se essa propriedade for definida como FALSE ou não utilizado, nenhum campo de cabeçalho X-MS-Exchange-organização-AutoForwarded será criado.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e9e0f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e9e0f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e9e0f-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="e9e0f-117">Protocol specifications</span></span>

<span data-ttu-id="e9e0f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9e0f-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9e0f-119">Define cada propriedade que é usada nos objetos que são descritos por prefixado MS-OXO documentos.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="e9e0f-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e9e0f-120">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e9e0f-121">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e9e0f-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e9e0f-122">Header files</span></span>

<span data-ttu-id="e9e0f-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9e0f-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9e0f-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9e0f-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9e0f-125">Mapitags.h</span></span>
  
> <span data-ttu-id="e9e0f-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="e9e0f-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9e0f-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9e0f-127">See also</span></span>



[<span data-ttu-id="e9e0f-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e9e0f-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9e0f-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="e9e0f-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9e0f-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e9e0f-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9e0f-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e9e0f-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

