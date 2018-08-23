---
title: Propriedade canônica PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f65c197999f23d959657cbfee9c6fbb0aaf439f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566282"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a><span data-ttu-id="03036-103">Propriedade canônica PidTagSearchRecipientEmailBcc</span><span class="sxs-lookup"><span data-stu-id="03036-103">PidTagSearchRecipientEmailBcc Canonical Property</span></span>

  
  
<span data-ttu-id="03036-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03036-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03036-105">Contém uma cadeia de caracteres Unicode que está sendo consultada na lista de endereços de email ou nomes de exibição dos destinatários abordados na linha **Cco** mensagens não enviadas no repositório.</span><span class="sxs-lookup"><span data-stu-id="03036-105">Contains a Unicode string that is being queried in the list of email addresses or display names of recipients addressed in the **BCC** line of unsent messages on the store.</span></span> 
  
## 

|||
|:-----|:-----|
|<span data-ttu-id="03036-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="03036-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="03036-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span><span class="sxs-lookup"><span data-stu-id="03036-107">PR_SEARCH_RECIP_EMAIL_BCC_W</span></span>  <br/> |
|<span data-ttu-id="03036-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="03036-108">Identifier:</span></span>  <br/> |<span data-ttu-id="03036-109">0x0EA8</span><span class="sxs-lookup"><span data-stu-id="03036-109">0x0EA8</span></span>  <br/> |
|<span data-ttu-id="03036-110">Tipo de propriedade:</span><span class="sxs-lookup"><span data-stu-id="03036-110">Property type:</span></span>  <br/> |<span data-ttu-id="03036-111">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="03036-111">PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="03036-112">Access:</span><span class="sxs-lookup"><span data-stu-id="03036-112">Access:</span></span>  <br/> |<span data-ttu-id="03036-113">Pesquisar</span><span class="sxs-lookup"><span data-stu-id="03036-113">Search</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03036-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="03036-114">Remarks</span></span>

<span data-ttu-id="03036-115">Essa propriedade só é relevante para mensagens no repositório que não tem sido enviadas, porque as mensagens que tenham sido enviadas ou recebidas não contêm informações Cco.</span><span class="sxs-lookup"><span data-stu-id="03036-115">This property is only relevant to messages on the store that have not been sent, because messages that have been sent or received do not contain BCC information.</span></span>
  
> [!NOTE]
> <span data-ttu-id="03036-116">Nesta marca de restrição de MAPI, usada durante a pesquisa de endereços de email ou nomes de exibição para o qual a mensagem será enviada como uma cópia carbono oculta, não pode ser definida no arquivo de cabeçalho para download que você possui atualmente.</span><span class="sxs-lookup"><span data-stu-id="03036-116">This MAPI restriction tag, used when searching for email addresses or display names to which the message will be sent as a blind carbon copy, might not be defined in the downloadable header file that you currently have.</span></span> <span data-ttu-id="03036-117">Você pode adicioná-la ao seu código usando o seguinte valor: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span><span class="sxs-lookup"><span data-stu-id="03036-117">You can add it to your code by using the following value: >  `#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="03036-118">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="03036-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="03036-119">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="03036-119">Protocol specifications</span></span>

<span data-ttu-id="03036-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03036-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03036-121">Fornece referências a relacionados especificações de protocolo do Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="03036-121">Provides references to related Microsoft Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="03036-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="03036-122">[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="03036-123">Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="03036-123">Specifies the properties and operations for manipulating a search folder list configuration.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="03036-124">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="03036-124">Header files</span></span>

<span data-ttu-id="03036-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="03036-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="03036-126">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="03036-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="03036-127">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="03036-127">Mapitags.h</span></span>
  
> <span data-ttu-id="03036-128">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="03036-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03036-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="03036-129">See also</span></span>



[<span data-ttu-id="03036-130">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="03036-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="03036-131">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="03036-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="03036-132">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="03036-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="03036-133">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="03036-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

