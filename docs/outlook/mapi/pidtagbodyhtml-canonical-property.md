---
title: Propriedade canônica PidTagBodyHtml
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagBodyHtml
api_type:
- HeaderDef
ms.assetid: 93b9215a-5900-411c-a0ae-6bba62cd5a1e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 19f0398d5e36cce13467a4fae86c4ea1d4019dd1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769013"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="a606e-103">Propriedade canônica PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="a606e-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="a606e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a606e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a606e-105">Contém a versão do idioma de marcação de hipertexto (HTML) do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a606e-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a606e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="a606e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a606e-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="a606e-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="a606e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="a606e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a606e-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="a606e-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="a606e-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="a606e-110">Data type:</span></span>  <br/> |<span data-ttu-id="a606e-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="a606e-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="a606e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="a606e-112">Area:</span></span>  <br/> |<span data-ttu-id="a606e-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="a606e-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a606e-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a606e-114">Remarks</span></span>

<span data-ttu-id="a606e-115">Essas propriedades contenham o mesmo texto da mensagem como **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mas em HTML.</span><span class="sxs-lookup"><span data-stu-id="a606e-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="a606e-116">Um armazenamento de mensagens que ofereça suporte a HTML indica, definindo o sinalizador **STORE_HTML_OK** no seu **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="a606e-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="a606e-117">**Observação** **STORE_HTML_OK** não está definido em versões do Mapidefs.h incluídos com o Microsoft® Exchange 2000 Server e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="a606e-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="a606e-118">Se **STORE_HTML_OK** é indefinido, use o valor 0x00010000.</span><span class="sxs-lookup"><span data-stu-id="a606e-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a606e-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="a606e-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a606e-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="a606e-120">Protocol specifications</span></span>

<span data-ttu-id="a606e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a606e-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a606e-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a606e-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a606e-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a606e-123">[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a606e-124">Trata objetos de mensagem e o anexo.</span><span class="sxs-lookup"><span data-stu-id="a606e-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a606e-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="a606e-125">Header files</span></span>

<span data-ttu-id="a606e-126">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a606e-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="a606e-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="a606e-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="a606e-128">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a606e-128">Mapitags.h</span></span>
  
> <span data-ttu-id="a606e-129">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="a606e-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a606e-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a606e-130">See also</span></span>



[<span data-ttu-id="a606e-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="a606e-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a606e-132">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="a606e-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a606e-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="a606e-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a606e-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="a606e-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

