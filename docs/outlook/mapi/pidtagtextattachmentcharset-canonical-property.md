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
ms.openlocfilehash: 1db41bc5c7ea71d65d892da520d4258354eb53cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358811"
---
# <a name="pidtagtextattachmentcharset-canonical-property"></a><span data-ttu-id="20a0f-103">Propriedade canônica PidTagTextAttachmentCharset</span><span class="sxs-lookup"><span data-stu-id="20a0f-103">PidTagTextAttachmentCharset Canonical Property</span></span>

  
  
<span data-ttu-id="20a0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20a0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20a0f-105">Contém o valor de conjunto de caracteres de um anexo de mensagem.</span><span class="sxs-lookup"><span data-stu-id="20a0f-105">Contains a message attachment's character set value.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="20a0f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="20a0f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="20a0f-107">Nenhum</span><span class="sxs-lookup"><span data-stu-id="20a0f-107">None</span></span>  <br/> |
|<span data-ttu-id="20a0f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="20a0f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="20a0f-109">0x371B</span><span class="sxs-lookup"><span data-stu-id="20a0f-109">0x371B</span></span>  <br/> |
|<span data-ttu-id="20a0f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="20a0f-110">Data type:</span></span>  <br/> |<span data-ttu-id="20a0f-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="20a0f-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="20a0f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="20a0f-112">Area:</span></span>  <br/> |<span data-ttu-id="20a0f-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="20a0f-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="20a0f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="20a0f-114">Remarks</span></span>

<span data-ttu-id="20a0f-115">Os dados dessa propriedade são derivados de um campo de título MIME do tipo conteúdo que começa com "text/", se um parâmetro "charset" estiver presente.</span><span class="sxs-lookup"><span data-stu-id="20a0f-115">This property's data is derived from a Content-Type MIME header field that starts with "text/", if a "charset" parameter is present.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="20a0f-116">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="20a0f-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="20a0f-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="20a0f-117">Protocol specifications</span></span>

<span data-ttu-id="20a0f-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="20a0f-118">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="20a0f-119">Converte de convenções de email padrão da Internet em objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="20a0f-119">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="20a0f-120">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="20a0f-120">Header files</span></span>

<span data-ttu-id="20a0f-121">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="20a0f-121">Mapidefs.h</span></span>
  
> <span data-ttu-id="20a0f-122">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="20a0f-122">Provides data type definitions.</span></span>
    
<span data-ttu-id="20a0f-123">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="20a0f-123">Mapitags.h</span></span>
  
> <span data-ttu-id="20a0f-124">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="20a0f-124">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="20a0f-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="20a0f-125">See also</span></span>



[<span data-ttu-id="20a0f-126">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="20a0f-126">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="20a0f-127">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="20a0f-127">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="20a0f-128">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="20a0f-128">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="20a0f-129">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="20a0f-129">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

