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
ms.openlocfilehash: 80d1fc3f711369471eb2c1473700f13a6b995594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578504"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="d0b72-103">Propriedade canônica PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="d0b72-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="d0b72-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d0b72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d0b72-105">Contém uma cadeia de caracteres Unicode que está sendo consultada no conteúdo de anexo no repositório.</span><span class="sxs-lookup"><span data-stu-id="d0b72-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="d0b72-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d0b72-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d0b72-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="d0b72-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="d0b72-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d0b72-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d0b72-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="d0b72-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="d0b72-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="d0b72-110">Property type:</span></span>  <br/> |<span data-ttu-id="d0b72-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d0b72-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d0b72-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d0b72-112">Area:</span></span>  <br/> |<span data-ttu-id="d0b72-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="d0b72-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="d0b72-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0b72-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="d0b72-115">Nesta marca de restrição de MAPI, usada quando você estiver procurando por conteúdo de anexo, não poderão ser definida no arquivo de cabeçalho para download que você possui atualmente.</span><span class="sxs-lookup"><span data-stu-id="d0b72-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="d0b72-116">Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="d0b72-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="d0b72-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d0b72-117">Protocol specifications</span></span>

<span data-ttu-id="d0b72-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0b72-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0b72-119">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d0b72-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d0b72-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d0b72-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d0b72-121">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d0b72-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d0b72-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d0b72-122">Header files</span></span>

<span data-ttu-id="d0b72-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d0b72-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d0b72-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d0b72-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d0b72-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d0b72-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d0b72-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d0b72-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d0b72-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="d0b72-127">See also</span></span>



[<span data-ttu-id="d0b72-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d0b72-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d0b72-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d0b72-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d0b72-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d0b72-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d0b72-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d0b72-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

