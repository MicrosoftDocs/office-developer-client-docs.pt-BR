---
title: Propriedade canônica PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7a9a5d090babce8105fab43bf8401448373777cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769449"
---
# <a name="pidtaglisthelp-canonical-property"></a><span data-ttu-id="f40fb-103">Propriedade canônica PidTagListHelp</span><span class="sxs-lookup"><span data-stu-id="f40fb-103">PidTagListHelp Canonical Property</span></span>

  
  
<span data-ttu-id="f40fb-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f40fb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f40fb-105">Contém o valor do campo de cabeçalho de uma mensagem de email extensões MIME (Multipurpose Internet) ajuda a lista.</span><span class="sxs-lookup"><span data-stu-id="f40fb-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Help header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f40fb-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="f40fb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f40fb-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span><span class="sxs-lookup"><span data-stu-id="f40fb-107">PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W</span></span>  <br/> |
|<span data-ttu-id="f40fb-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="f40fb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f40fb-109">0x1043</span><span class="sxs-lookup"><span data-stu-id="f40fb-109">0x1043</span></span>  <br/> |
|<span data-ttu-id="f40fb-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="f40fb-110">Data type:</span></span>  <br/> |<span data-ttu-id="f40fb-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f40fb-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="f40fb-112">Área:</span><span class="sxs-lookup"><span data-stu-id="f40fb-112">Area:</span></span>  <br/> |<span data-ttu-id="f40fb-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="f40fb-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f40fb-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f40fb-114">Remarks</span></span>

<span data-ttu-id="f40fb-115">Para gerar um campo de cabeçalho de lista-Help, clientes devem definir o valor de **PR_LIST_HELP** ou uma propriedade associada com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="f40fb-115">To generate a List-Help header field, clients must set the value of **PR_LIST_HELP** or an associated property to the desired value.</span></span> <span data-ttu-id="f40fb-116">Os autores MIME devem copiar esse valor no campo de cabeçalho de lista-Help.</span><span class="sxs-lookup"><span data-stu-id="f40fb-116">MIME writers must copy this value to the List-Help header field.</span></span> 
  
<span data-ttu-id="f40fb-117">Para definir o valor dessas propriedades relacionadas ao servidor de lista, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir:</span><span class="sxs-lookup"><span data-stu-id="f40fb-117">To set the value of these list server-related properties, MIME clients must write the header fields as specified in the following table:</span></span>
  
|<span data-ttu-id="f40fb-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="f40fb-118">**Property**</span></span>|<span data-ttu-id="f40fb-119">**Nome do campo de cabeçalho preferencial**</span><span class="sxs-lookup"><span data-stu-id="f40fb-119">**Preferred header field name**</span></span>|<span data-ttu-id="f40fb-120">**Nome do campo de cabeçalho alternativo**</span><span class="sxs-lookup"><span data-stu-id="f40fb-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f40fb-121">**PR_LIST_HELP**</span><span class="sxs-lookup"><span data-stu-id="f40fb-121">**PR_LIST_HELP**</span></span> <br/> |<span data-ttu-id="f40fb-122">Lista-Help</span><span class="sxs-lookup"><span data-stu-id="f40fb-122">List-Help</span></span>  <br/> |<span data-ttu-id="f40fb-123">X-lista-Help</span><span class="sxs-lookup"><span data-stu-id="f40fb-123">X-List-Help</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="f40fb-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="f40fb-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f40fb-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="f40fb-125">Protocol specifications</span></span>

<span data-ttu-id="f40fb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f40fb-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f40fb-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="f40fb-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f40fb-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f40fb-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f40fb-129">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f40fb-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f40fb-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f40fb-130">Header files</span></span>

<span data-ttu-id="f40fb-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f40fb-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f40fb-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="f40fb-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f40fb-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f40fb-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f40fb-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="f40fb-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f40fb-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f40fb-135">See also</span></span>



[<span data-ttu-id="f40fb-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="f40fb-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f40fb-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="f40fb-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f40fb-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="f40fb-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f40fb-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="f40fb-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

