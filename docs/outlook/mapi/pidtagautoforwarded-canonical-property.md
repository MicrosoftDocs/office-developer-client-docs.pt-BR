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
ms.openlocfilehash: 25d1bb121df6470f5038a2106587e3f5b37f6bb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326611"
---
# <a name="pidtagautoforwarded-canonical-property"></a><span data-ttu-id="27e35-103">Propriedade canônica PidTagAutoForwarded</span><span class="sxs-lookup"><span data-stu-id="27e35-103">PidTagAutoForwarded Canonical Property</span></span>

  
  
<span data-ttu-id="27e35-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27e35-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27e35-105">Contém TRUE se o cliente solicita um campo de header X-MS-Exchange-Organization-AutoForwarded.</span><span class="sxs-lookup"><span data-stu-id="27e35-105">Contains TRUE if the client requests an X-MS-Exchange-Organization-AutoForwarded header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="27e35-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="27e35-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="27e35-107">PR_AUTO_FORWARDED</span><span class="sxs-lookup"><span data-stu-id="27e35-107">PR_AUTO_FORWARDED</span></span>  <br/> |
|<span data-ttu-id="27e35-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="27e35-108">Identifier:</span></span>  <br/> |<span data-ttu-id="27e35-109">0x0005</span><span class="sxs-lookup"><span data-stu-id="27e35-109">0x0005</span></span>  <br/> |
|<span data-ttu-id="27e35-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="27e35-110">Data type:</span></span>  <br/> |<span data-ttu-id="27e35-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="27e35-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="27e35-112">Área:</span><span class="sxs-lookup"><span data-stu-id="27e35-112">Area:</span></span>  <br/> |<span data-ttu-id="27e35-113">Relatórios gerais</span><span class="sxs-lookup"><span data-stu-id="27e35-113">General reporting</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="27e35-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="27e35-114">Remarks</span></span>

<span data-ttu-id="27e35-115">Se essa propriedade for definida como FALSE ou não for usada, nenhum campo de header X-MS-Exchange-Organization-AutoForwarded será criado.</span><span class="sxs-lookup"><span data-stu-id="27e35-115">If this property is set to FALSE or not used, no X-MS-Exchange-Organization-AutoForwarded header field will be created.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="27e35-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="27e35-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="27e35-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="27e35-117">Protocol specifications</span></span>

<span data-ttu-id="27e35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27e35-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27e35-119">Define cada propriedade que é usada nos objetos descritos por documentos prefixados por MS-OXO.</span><span class="sxs-lookup"><span data-stu-id="27e35-119">Defines each property that is used in the objects that are described by MS-OXO-prefixed documents.</span></span>
    
<span data-ttu-id="27e35-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="27e35-120">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="27e35-121">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="27e35-121">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="27e35-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="27e35-122">Header files</span></span>

<span data-ttu-id="27e35-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="27e35-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="27e35-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="27e35-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="27e35-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="27e35-125">Mapitags.h</span></span>
  
> <span data-ttu-id="27e35-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="27e35-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="27e35-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="27e35-127">See also</span></span>



[<span data-ttu-id="27e35-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="27e35-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="27e35-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="27e35-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="27e35-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="27e35-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="27e35-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="27e35-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

