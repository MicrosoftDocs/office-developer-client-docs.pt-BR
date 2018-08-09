---
title: Propriedade canônica PidLidCategories
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCategories
api_type:
- COM
ms.assetid: 6ad2aedc-405b-475e-ac76-7ecbbef28f73
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 01d4391850067d00645b5c0248e1bf858c2a9049
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768332"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="190cf-103">Propriedade canônica PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="190cf-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="190cf-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="190cf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="190cf-105">Especifica uma lista de categorias para um item.</span><span class="sxs-lookup"><span data-stu-id="190cf-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="190cf-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="190cf-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="190cf-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="190cf-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="190cf-108">Propriedade definida:</span><span class="sxs-lookup"><span data-stu-id="190cf-108">Property set:</span></span>  <br/> |<span data-ttu-id="190cf-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="190cf-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="190cf-110">ID de longo (LID):</span><span class="sxs-lookup"><span data-stu-id="190cf-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="190cf-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="190cf-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="190cf-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="190cf-112">Data type:</span></span>  <br/> |<span data-ttu-id="190cf-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="190cf-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="190cf-114">Área:</span><span class="sxs-lookup"><span data-stu-id="190cf-114">Area:</span></span>  <br/> |<span data-ttu-id="190cf-115">Comuns</span><span class="sxs-lookup"><span data-stu-id="190cf-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="190cf-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="190cf-116">Remarks</span></span>

<span data-ttu-id="190cf-117">Para gerar um campo de cabeçalho de palavras-chave, os clientes devem definir o valor dessa propriedade para os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="190cf-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="190cf-118">Esta propriedade tem várias cadeias de caracteres; cada categoria deve ser mapeada para uma única palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="190cf-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="190cf-119">Escritores de Multipurpose Internet Mail Extensions (MIME) devem copiar cada valor sub-recurso dessa propriedade para uma palavra-chave separada no campo de cabeçalho de palavras-chave, com uma vírgula (U + 002 C) e (U + 0020) de espaço separando cada palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="190cf-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="190cf-120">Os autores MIME poderão perder essa propriedade em vez de copiá-lo para o campo de cabeçalho de palavras-chave, para evitar conflitos entre conjuntos diferentes das categorias em organizações diferentes.</span><span class="sxs-lookup"><span data-stu-id="190cf-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="190cf-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="190cf-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="190cf-122">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="190cf-122">Protocol specifications</span></span>

<span data-ttu-id="190cf-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190cf-123">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190cf-124">Fornece a definição de propriedade do conjunto e referências para relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="190cf-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="190cf-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="190cf-125">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="190cf-126">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="190cf-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="190cf-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="190cf-127">Header files</span></span>

<span data-ttu-id="190cf-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="190cf-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="190cf-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="190cf-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="190cf-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="190cf-130">See also</span></span>



[<span data-ttu-id="190cf-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="190cf-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="190cf-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="190cf-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="190cf-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="190cf-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="190cf-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="190cf-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

