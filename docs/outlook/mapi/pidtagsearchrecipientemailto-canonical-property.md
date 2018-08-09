---
title: Propriedade canônica PidTagSearchRecipientEmailTo
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f5de77c3-5912-f7bc-8e8c-3a053545c359
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5d6c029ba91b6b3489d3f6544ead6788760363a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769989"
---
# <a name="pidtagsearchrecipientemailto-canonical-property"></a><span data-ttu-id="1f259-103">Propriedade canônica PidTagSearchRecipientEmailTo</span><span class="sxs-lookup"><span data-stu-id="1f259-103">PidTagSearchRecipientEmailTo Canonical Property</span></span>

  
  
<span data-ttu-id="1f259-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1f259-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1f259-105">Contém uma cadeia de caracteres Unicode que está sendo consultada na lista de endereços de email ou nomes de exibição dos destinatários que serão abordados na linha **para** das mensagens no repositório.</span><span class="sxs-lookup"><span data-stu-id="1f259-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients that are addressed in the **To** line of messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="1f259-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="1f259-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="1f259-107">PR_SEARCH_RECIP_EMAIL_TO_W</span><span class="sxs-lookup"><span data-stu-id="1f259-107">PR_SEARCH_RECIP_EMAIL_TO_W</span></span>  <br/> |
|<span data-ttu-id="1f259-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="1f259-108">Identifier:</span></span>  <br/> |<span data-ttu-id="1f259-109">0x0EA6</span><span class="sxs-lookup"><span data-stu-id="1f259-109">0x0EA6</span></span>  <br/> |
|<span data-ttu-id="1f259-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="1f259-110">Property type:</span></span>  <br/> |<span data-ttu-id="1f259-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1f259-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="1f259-112">Área:</span><span class="sxs-lookup"><span data-stu-id="1f259-112">Area:</span></span>  <br/> |<span data-ttu-id="1f259-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="1f259-113">Search</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="1f259-114">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f259-114">Related resources</span></span>

> [!NOTE]
> <span data-ttu-id="1f259-115">Nesta marca de restrição de MAPI, usada quando você procurar endereços de email ou exibe nomes para o qual a mensagem é enviada, não poderão ser definida no arquivo de cabeçalho para download que você possui atualmente.</span><span class="sxs-lookup"><span data-stu-id="1f259-115">This MAPI restriction tag, used when you search for email addresses or display names to which the message is sent, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="1f259-116">Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span><span class="sxs-lookup"><span data-stu-id="1f259-116">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_TO_W PROP_TAG(PT_UNICODE, 0x0EA6)`</span></span>
  
### <a name="protocol-specifications"></a><span data-ttu-id="1f259-117">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="1f259-117">Protocol specifications</span></span>

<span data-ttu-id="1f259-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f259-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f259-119">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="1f259-119">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="1f259-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1f259-120">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="1f259-121">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="1f259-121">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="1f259-122">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1f259-122">Header files</span></span>

<span data-ttu-id="1f259-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1f259-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="1f259-124">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="1f259-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="1f259-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="1f259-125">Mapitags.h</span></span>
  
> <span data-ttu-id="1f259-126">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="1f259-126">Contains definitions of properties that are listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1f259-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f259-127">See also</span></span>



[<span data-ttu-id="1f259-128">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="1f259-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="1f259-129">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="1f259-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="1f259-130">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="1f259-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="1f259-131">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="1f259-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

