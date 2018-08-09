---
title: Propriedade canônica PidTagTextAttachmentCharset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagTextAttachmentCharset
api_type:
- COM
ms.assetid: d347c949-d0c3-4a36-8447-3fa01111cdc1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c728799832b10ad2d4533a9a040582b67054baad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770134"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="fe7b2-103">Propriedade canônica PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="fe7b2-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="fe7b2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fe7b2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fe7b2-105">Contém o valor de conjunto de caracteres do anexo da mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe7b2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="fe7b2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fe7b2-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="fe7b2-107">None</span></span>  <br/> |
|<span data-ttu-id="fe7b2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="fe7b2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fe7b2-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="fe7b2-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="fe7b2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="fe7b2-110">Data type:</span></span>  <br/> |<span data-ttu-id="fe7b2-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="fe7b2-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="fe7b2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="fe7b2-112">Area:</span></span>  <br/> |<span data-ttu-id="fe7b2-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="fe7b2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe7b2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe7b2-114">Remarks</span></span>

<span data-ttu-id="fe7b2-115">Dados dessa propriedade são derivados de um campo de cabeçalho de tipo de conteúdo MIME que começa com "text /", se houver um parâmetro "charset".</span><span class="sxs-lookup"><span data-stu-id="fe7b2-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="fe7b2-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="fe7b2-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fe7b2-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="fe7b2-117">Protocol specifications</span></span>

<span data-ttu-id="fe7b2-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fe7b2-118">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fe7b2-119">Converte de convenções de email padrão da Internet para os objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fe7b2-120">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe7b2-120">Header files</span></span>

<span data-ttu-id="fe7b2-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fe7b2-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="fe7b2-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="fe7b2-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="fe7b2-123">Mapitags.h</span></span>
  
> <span data-ttu-id="fe7b2-124">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="fe7b2-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fe7b2-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe7b2-125">See also</span></span>



[<span data-ttu-id="fe7b2-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="fe7b2-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fe7b2-127">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="fe7b2-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fe7b2-128">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="fe7b2-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fe7b2-129">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="fe7b2-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

