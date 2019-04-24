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
ms.openlocfilehash: 6ed59228ee06a1d3e362115a99bf4b859dfeb698
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359042"
---
# <a name="pidtagbodyhtml-canonical-property"></a><span data-ttu-id="c6617-103">Propriedade canônica PidTagBodyHtml</span><span class="sxs-lookup"><span data-stu-id="c6617-103">PidTagBodyHtml Canonical Property</span></span>

  
  
<span data-ttu-id="c6617-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c6617-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c6617-105">Contém a versão do HTML (Hypertext Markup Language) do texto da mensagem.</span><span class="sxs-lookup"><span data-stu-id="c6617-105">Contains the Hypertext Markup Language (HTML) version of the message text.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c6617-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="c6617-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c6617-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span><span class="sxs-lookup"><span data-stu-id="c6617-107">PR_BODY_HTML, PR_BODY_HTML_A, PR_BODY_HTML_W</span></span>  <br/> |
|<span data-ttu-id="c6617-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="c6617-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c6617-109">0x1013</span><span class="sxs-lookup"><span data-stu-id="c6617-109">0x1013</span></span>  <br/> |
|<span data-ttu-id="c6617-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="c6617-110">Data type:</span></span>  <br/> |<span data-ttu-id="c6617-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="c6617-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="c6617-112">Área:</span><span class="sxs-lookup"><span data-stu-id="c6617-112">Area:</span></span>  <br/> |<span data-ttu-id="c6617-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="c6617-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6617-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c6617-114">Remarks</span></span>

<span data-ttu-id="c6617-115">Essas propriedades contêm o mesmo texto de mensagem que o **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), mas em HTML.</span><span class="sxs-lookup"><span data-stu-id="c6617-115">These properties contain the same message text as the **PR_BODY_CONTENT_LOCATION** ([PidTagBodyContentLocation](pidtagbodycontentlocation-canonical-property.md)), but in HTML.</span></span> 
  
<span data-ttu-id="c6617-116">Um repositório de mensagens que oferece suporte a HTML indica isso Configurando o sinalizador **STORE_HTML_OK** em seu **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c6617-116">A message store that supports HTML indicates this by setting the **STORE_HTML_OK** flag in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)).</span></span> 
  
 <span data-ttu-id="c6617-117">**Observação** O **STORE_HTML_OK** não está definido nas versões do mapidefs. h incluídas no Microsoft ® Exchange 2000 Server e versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="c6617-117">**Note** **STORE_HTML_OK** is not defined in versions of Mapidefs.h included with Microsoft® Exchange 2000 Server and earlier.</span></span> <span data-ttu-id="c6617-118">Se **STORE_HTML_OK** estiver indefinido, use o valor 0x00010000 em vez disso.</span><span class="sxs-lookup"><span data-stu-id="c6617-118">If **STORE_HTML_OK** is undefined, use the value 0x00010000 instead.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="c6617-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6617-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c6617-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="c6617-120">Protocol specifications</span></span>

<span data-ttu-id="c6617-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6617-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6617-122">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="c6617-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c6617-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c6617-123">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c6617-124">Manipula objetos Message e Attachment.</span><span class="sxs-lookup"><span data-stu-id="c6617-124">Handles message and attachment objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c6617-125">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c6617-125">Header files</span></span>

<span data-ttu-id="c6617-126">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="c6617-126">Mapidefs.h</span></span>
  
> <span data-ttu-id="c6617-127">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="c6617-127">Provides data type definitions.</span></span>
    
<span data-ttu-id="c6617-128">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="c6617-128">Mapitags.h</span></span>
  
> <span data-ttu-id="c6617-129">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="c6617-129">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c6617-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6617-130">See also</span></span>



[<span data-ttu-id="c6617-131">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="c6617-131">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c6617-132">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="c6617-132">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c6617-133">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="c6617-133">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c6617-134">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="c6617-134">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

