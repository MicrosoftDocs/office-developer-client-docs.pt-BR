---
title: Propriedade canônica PidTagListSubscribe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListSubscribe
api_type:
- HeaderDef
ms.assetid: 97387a82-8e40-4c76-818c-2229fac12e01
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5030e48ac87408f983696a365d3234c3362346c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769442"
---
# <a name="pidtaglistsubscribe-canonical-property"></a><span data-ttu-id="ddd60-103">Propriedade canônica PidTagListSubscribe</span><span class="sxs-lookup"><span data-stu-id="ddd60-103">PidTagListSubscribe Canonical Property</span></span>

  
  
<span data-ttu-id="ddd60-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddd60-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddd60-105">Contém o valor do campo de cabeçalho de assinar a lista de uma mensagem de email extensões MIME (Multipurpose Internet).</span><span class="sxs-lookup"><span data-stu-id="ddd60-105">Contains the value of a Multipurpose Internet Mail Extensions (MIME) message's List-Subscribe header field.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ddd60-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="ddd60-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ddd60-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span><span class="sxs-lookup"><span data-stu-id="ddd60-107">PR_LIST_SUBSCRIBE, PR_LIST_SUBSCRIBE_A, PR_LIST_SUBSCRIBE_W</span></span>  <br/> |
|<span data-ttu-id="ddd60-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="ddd60-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ddd60-109">0x1044</span><span class="sxs-lookup"><span data-stu-id="ddd60-109">0x1044</span></span>  <br/> |
|<span data-ttu-id="ddd60-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="ddd60-110">Data type:</span></span>  <br/> |<span data-ttu-id="ddd60-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="ddd60-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="ddd60-112">Área:</span><span class="sxs-lookup"><span data-stu-id="ddd60-112">Area:</span></span>  <br/> |<span data-ttu-id="ddd60-113">Diversos</span><span class="sxs-lookup"><span data-stu-id="ddd60-113">Miscellaneous</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddd60-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddd60-114">Remarks</span></span>

<span data-ttu-id="ddd60-115">Para gerar um campo de cabeçalho se inscrever lista, os clientes devem definir o valor dessas propriedades com o valor desejado.</span><span class="sxs-lookup"><span data-stu-id="ddd60-115">To generate a List-Subscribe header field, clients must set the value of these properties to the desired value.</span></span> <span data-ttu-id="ddd60-116">Os autores MIME devem copiar o valor dessas propriedades no campo de cabeçalho assine a lista.</span><span class="sxs-lookup"><span data-stu-id="ddd60-116">MIME writers must copy the value of these properties to the List-Subscribe header field.</span></span>
  
<span data-ttu-id="ddd60-117">Para definir o valor das propriedades relacionadas ao servidor como essas, os clientes MIME devem gravar os campos de cabeçalho, conforme especificado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ddd60-117">To set the value of server-related properties like these, MIME clients must write the header fields as specified in the following table.</span></span>
  
|<span data-ttu-id="ddd60-118">**Propriedade**</span><span class="sxs-lookup"><span data-stu-id="ddd60-118">**Property**</span></span>|<span data-ttu-id="ddd60-119">**Nome do campo de cabeçalho preferencial**</span><span class="sxs-lookup"><span data-stu-id="ddd60-119">**Preferred header field name**</span></span>|<span data-ttu-id="ddd60-120">**Nome do campo de cabeçalho alternativo**</span><span class="sxs-lookup"><span data-stu-id="ddd60-120">**Alternate header field name**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ddd60-121">**PidTagListSubscribe**</span><span class="sxs-lookup"><span data-stu-id="ddd60-121">**PidTagListSubscribe**</span></span> <br/> |<span data-ttu-id="ddd60-122">Assine a lista</span><span class="sxs-lookup"><span data-stu-id="ddd60-122">List-Subscribe</span></span>  <br/> |<span data-ttu-id="ddd60-123">Inscrever-se lista X</span><span class="sxs-lookup"><span data-stu-id="ddd60-123">X-List-Subscribe</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ddd60-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="ddd60-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ddd60-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="ddd60-125">Protocol specifications</span></span>

<span data-ttu-id="ddd60-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddd60-126">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddd60-127">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ddd60-127">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ddd60-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ddd60-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ddd60-129">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="ddd60-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ddd60-130">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ddd60-130">Header files</span></span>

<span data-ttu-id="ddd60-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ddd60-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="ddd60-132">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="ddd60-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="ddd60-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ddd60-133">Mapitags.h</span></span>
  
> <span data-ttu-id="ddd60-134">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="ddd60-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ddd60-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddd60-135">See also</span></span>



[<span data-ttu-id="ddd60-136">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd60-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ddd60-137">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="ddd60-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ddd60-138">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="ddd60-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ddd60-139">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="ddd60-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

