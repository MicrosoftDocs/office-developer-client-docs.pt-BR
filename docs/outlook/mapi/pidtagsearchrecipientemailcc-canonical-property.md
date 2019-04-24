---
title: Propriedade canônica PidTagSearchRecipientEmailCc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 38fe217d-cf2e-51de-c97a-acb015129fd3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 03501e14740d7b27bd54d761ae701e8863ad79dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358944"
---
# <a name="pidtagsearchrecipientemailcc-canonical-property"></a><span data-ttu-id="784a8-103">Propriedade canônica PidTagSearchRecipientEmailCc</span><span class="sxs-lookup"><span data-stu-id="784a8-103">PidTagSearchRecipientEmailCc Canonical Property</span></span>

  
  
<span data-ttu-id="784a8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="784a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="784a8-105">Contém uma cadeia de caracteres Unicode que está sendo consultada na lista de endereços de email ou nomes de exibição de destinatários tratados na linha **CC** das mensagens no repositório.</span><span class="sxs-lookup"><span data-stu-id="784a8-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **CC** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="784a8-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="784a8-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="784a8-107">PR_SEARCH_RECIP_EMAIL_CC_W</span><span class="sxs-lookup"><span data-stu-id="784a8-107">PR_SEARCH_RECIP_EMAIL_CC_W</span></span>  <br/> |
|<span data-ttu-id="784a8-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="784a8-108">Identifier:</span></span>  <br/> |<span data-ttu-id="784a8-109">0x0EA7</span><span class="sxs-lookup"><span data-stu-id="784a8-109">0x0EA7</span></span>  <br/> |
|<span data-ttu-id="784a8-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="784a8-110">Property type:</span></span>  <br/> |<span data-ttu-id="784a8-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="784a8-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="784a8-112">Área:</span><span class="sxs-lookup"><span data-stu-id="784a8-112">Area:</span></span>  <br/> |<span data-ttu-id="784a8-113">Pesquisa</span><span class="sxs-lookup"><span data-stu-id="784a8-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="784a8-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="784a8-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="784a8-115">Essa marca de restrição de MAPI, usada quando você pesquisa endereços de email ou nomes de exibição para os quais a mensagem é enviada como uma cópia carbono, pode não ser definida no arquivo de cabeçalho baixável que você tem no momento.</span><span class="sxs-lookup"><span data-stu-id="784a8-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent as a carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="784a8-116">Você pode adicioná-lo ao seu código usando o seguinte valor: >`#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span><span class="sxs-lookup"><span data-stu-id="784a8-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_CC_W PROP_TAG(PT_UNICODE, 0x0EA7)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="784a8-117">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="784a8-117">Protocol specifications</span></span>

<span data-ttu-id="784a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784a8-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784a8-119">Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.</span><span class="sxs-lookup"><span data-stu-id="784a8-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="784a8-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="784a8-120">[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="784a8-121">Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="784a8-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="784a8-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="784a8-122">Header files</span></span>

<span data-ttu-id="784a8-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="784a8-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="784a8-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="784a8-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="784a8-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="784a8-125">Mapitags.h</span></span>
  
> <span data-ttu-id="784a8-126">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="784a8-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="784a8-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="784a8-127">See also</span></span>



[<span data-ttu-id="784a8-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="784a8-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="784a8-129">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="784a8-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="784a8-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="784a8-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="784a8-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="784a8-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

