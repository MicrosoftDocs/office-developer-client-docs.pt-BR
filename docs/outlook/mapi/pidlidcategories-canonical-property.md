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
ms.openlocfilehash: b2047f04f3f4a8d2b3e58e07a71e7e2463eff9cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344972"
---
# <a name="pidlidcategories-canonical-property"></a><span data-ttu-id="e7877-103">Propriedade canônica PidLidCategories</span><span class="sxs-lookup"><span data-stu-id="e7877-103">PidLidCategories Canonical Property</span></span>

  
  
<span data-ttu-id="e7877-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e7877-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e7877-105">Especifica uma lista de categorias para um item.</span><span class="sxs-lookup"><span data-stu-id="e7877-105">Specifies a list of categories for an item.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e7877-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e7877-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e7877-107">dispidCategories</span><span class="sxs-lookup"><span data-stu-id="e7877-107">dispidCategories</span></span>  <br/> |
|<span data-ttu-id="e7877-108">Conjunto de propriedades:</span><span class="sxs-lookup"><span data-stu-id="e7877-108">Property set:</span></span>  <br/> |<span data-ttu-id="e7877-109">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="e7877-109">PS_PUBLIC_STRINGS</span></span>  <br/> |
|<span data-ttu-id="e7877-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="e7877-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="e7877-111">0x00002328</span><span class="sxs-lookup"><span data-stu-id="e7877-111">0x00002328</span></span>  <br/> |
|<span data-ttu-id="e7877-112">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e7877-112">Data type:</span></span>  <br/> |<span data-ttu-id="e7877-113">PT_MV_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e7877-113">PT_MV_UNICODE</span></span>  <br/> |
|<span data-ttu-id="e7877-114">Área:</span><span class="sxs-lookup"><span data-stu-id="e7877-114">Area:</span></span>  <br/> |<span data-ttu-id="e7877-115">Comum</span><span class="sxs-lookup"><span data-stu-id="e7877-115">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7877-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7877-116">Remarks</span></span>

<span data-ttu-id="e7877-117">Para gerar um campo de cabeçalho keywords, os clientes devem definir o valor dessa propriedade para os valores desejados.</span><span class="sxs-lookup"><span data-stu-id="e7877-117">To generate a keywords header field, clients must set the value of this property to the desired values.</span></span> <span data-ttu-id="e7877-118">Essa propriedade tem várias cadeias de caracteres; cada categoria deve ser mapeada para uma única palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="e7877-118">This property has multiple strings; each category should be mapped to a single keyword.</span></span>
  
<span data-ttu-id="e7877-119">Os gravadores de MIME (Multipurpose Internet Mail Extensions) devem copiar cada subvalor dessa propriedade para uma palavra-chave separada no campo de cabeçalho keywords, com uma vírgula (U + 002C) e espaço (U + 0020) separando cada palavra-chave.</span><span class="sxs-lookup"><span data-stu-id="e7877-119">Multipurpose Internet Mail Extensions (MIME) writers should copy each sub-value of this property to a separate keyword in the Keywords header field, with a comma (U+002C) and space (U+0020) separating each keyword.</span></span> <span data-ttu-id="e7877-120">Os gravadores MIME podem descartar essa propriedade em vez de copiá-la para o campo de cabeçalho keywords, a fim de evitar o conflito entre diferentes conjuntos de categorias em diferentes organizações.</span><span class="sxs-lookup"><span data-stu-id="e7877-120">MIME writers may drop this property instead of copying it to the keywords header field, in order to avoid conflict among different sets of categories in different organizations.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e7877-121">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7877-121">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e7877-122">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="e7877-122">Protocol specifications</span></span>

<span data-ttu-id="e7877-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7877-123">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7877-124">Fornece definição e referências de conjunto de propriedades para especificações de protocolo do Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="e7877-124">Provides property set definition and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e7877-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e7877-125">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e7877-126">Converte as convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e7877-126">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e7877-127">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e7877-127">Header files</span></span>

<span data-ttu-id="e7877-128">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e7877-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="e7877-129">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e7877-129">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e7877-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="e7877-130">See also</span></span>



[<span data-ttu-id="e7877-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e7877-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e7877-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e7877-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e7877-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e7877-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e7877-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e7877-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

