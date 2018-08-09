---
title: Propriedade canônica PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 008dd69f5e31b601b678a4346880e6b3c89a0f39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769976"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="6125d-103">Propriedade canônica PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="6125d-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="6125d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6125d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6125d-105">Contém uma cadeia de caracteres Unicode que está sendo consultada no conteúdo de anexo no repositório.</span><span class="sxs-lookup"><span data-stu-id="6125d-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="6125d-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="6125d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6125d-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="6125d-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="6125d-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="6125d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6125d-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="6125d-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="6125d-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="6125d-110">Property type:</span></span>  <br/> |<span data-ttu-id="6125d-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6125d-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6125d-112">Área:</span><span class="sxs-lookup"><span data-stu-id="6125d-112">Area:</span></span>  <br/> |<span data-ttu-id="6125d-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="6125d-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="6125d-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="6125d-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="6125d-115">Nesta marca de restrição de MAPI, usada quando você estiver procurando por conteúdo de anexo, não poderão ser definida no arquivo de cabeçalho para download que você possui atualmente.</span><span class="sxs-lookup"><span data-stu-id="6125d-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="6125d-116">Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="6125d-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="6125d-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="6125d-117">Protocol specifications</span></span>

<span data-ttu-id="6125d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6125d-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6125d-119">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="6125d-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6125d-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6125d-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6125d-121">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="6125d-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6125d-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6125d-122">Header files</span></span>

<span data-ttu-id="6125d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6125d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="6125d-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="6125d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="6125d-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6125d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="6125d-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="6125d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6125d-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6125d-127">See also</span></span>



[<span data-ttu-id="6125d-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="6125d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6125d-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="6125d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6125d-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="6125d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6125d-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="6125d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)
