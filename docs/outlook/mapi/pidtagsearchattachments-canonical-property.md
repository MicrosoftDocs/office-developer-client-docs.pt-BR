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
ms.openlocfilehash: 95729474db29fe21f808ec5c8f571bec4600db70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336320"
---
# <a name="pidtagsearchattachments-canonical-property"></a><span data-ttu-id="4780e-103">Propriedade canônica PidTagSearchAttachments</span><span class="sxs-lookup"><span data-stu-id="4780e-103">PidTagSearchAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="4780e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4780e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4780e-105">Contém uma cadeia de caracteres Unicode que está sendo consultada no conteúdo do anexo no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4780e-105">Contains a Unicode string that is being queried in attachment contents on the store.</span></span>
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="4780e-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="4780e-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4780e-107">PR_SEARCH_ATTACHMENTS_W</span><span class="sxs-lookup"><span data-stu-id="4780e-107">PR_SEARCH_ATTACHMENTS_W</span></span>  <br/> |
|<span data-ttu-id="4780e-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="4780e-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4780e-109">0x0EA5</span><span class="sxs-lookup"><span data-stu-id="4780e-109">0x0EA5</span></span>  <br/> |
|<span data-ttu-id="4780e-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="4780e-110">Property type:</span></span>  <br/> |<span data-ttu-id="4780e-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4780e-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="4780e-112">Área:</span><span class="sxs-lookup"><span data-stu-id="4780e-112">Area:</span></span>  <br/> |<span data-ttu-id="4780e-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="4780e-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="4780e-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="4780e-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="4780e-115">Essa marca de restrição MAPI, usada quando você está procurando conteúdo de anexo, pode não ser definida no arquivo de título baixável que você tem no momento.</span><span class="sxs-lookup"><span data-stu-id="4780e-115">This MAPI restriction tag, used when you are searching for attachment contents, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="4780e-116">Você pode adicioná-lo ao seu código usando o seguinte valor: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span><span class="sxs-lookup"><span data-stu-id="4780e-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="4780e-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="4780e-117">Protocol specifications</span></span>

<span data-ttu-id="4780e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4780e-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4780e-119">Fornece referências a especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4780e-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4780e-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4780e-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4780e-121">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="4780e-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4780e-122">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="4780e-122">Header files</span></span>

<span data-ttu-id="4780e-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4780e-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="4780e-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4780e-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="4780e-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="4780e-125">Mapitags.h</span></span>
  
> <span data-ttu-id="4780e-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="4780e-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4780e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4780e-127">See also</span></span>



[<span data-ttu-id="4780e-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="4780e-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4780e-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="4780e-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4780e-130">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="4780e-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4780e-131">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="4780e-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

