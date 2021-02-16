---
title: Propriedade canônica PidTagOriginalAuthorEmailAddress
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorEmailAddress
api_type:
- COM
ms.assetid: 67cda756-ba71-4f29-a601-55359e44d93b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7918c5d5b585ffb199bfbc140edfb8286b499b40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436164"
---
# <a name="pidtagoriginalauthoremailaddress-canonical-property"></a><span data-ttu-id="d7768-103">Propriedade canônica PidTagOriginalAuthorEmailAddress</span><span class="sxs-lookup"><span data-stu-id="d7768-103">PidTagOriginalAuthorEmailAddress Canonical Property</span></span>

  
  
<span data-ttu-id="d7768-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d7768-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d7768-105">Contém o endereço de email do autor da primeira versão de uma mensagem, ou seja, a mensagem antes de ser encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="d7768-105">Contains the email address of the author of the first version of a message, that is, the message before being forwarded or replied to.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d7768-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d7768-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d7768-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span><span class="sxs-lookup"><span data-stu-id="d7768-107">PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_A, PR_ORIGINAL_AUTHOR_EMAIL_ADDRESS_W</span></span>  <br/> |
|<span data-ttu-id="d7768-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d7768-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d7768-109">0x007A</span><span class="sxs-lookup"><span data-stu-id="d7768-109">0x007A</span></span>  <br/> |
|<span data-ttu-id="d7768-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d7768-110">Data type:</span></span>  <br/> |<span data-ttu-id="d7768-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d7768-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="d7768-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d7768-112">Area:</span></span>  <br/> |<span data-ttu-id="d7768-113">Servidor</span><span class="sxs-lookup"><span data-stu-id="d7768-113">Server</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7768-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7768-114">Remarks</span></span>

<span data-ttu-id="d7768-115">Essas propriedades são exemplos das propriedades de endereço do autor de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="d7768-115">These properties are examples of the address properties for the author of a message.</span></span> <span data-ttu-id="d7768-116">No primeiro envio da mensagem, o aplicativo cliente deve definir essas propriedades como o valor da propriedade **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="d7768-116">At first submission of the message, the client application should set these properties to the value of the **PR_SENDER_EMAIL_ADDRESS** ([PidTagSenderEmailAddress](pidtagsenderemailaddress-canonical-property.md)) property.</span></span> <span data-ttu-id="d7768-117">Ela nunca é alterada quando a mensagem é encaminhada ou respondida.</span><span class="sxs-lookup"><span data-stu-id="d7768-117">It is never changed when the message is forwarded or replied to.</span></span>
  
<span data-ttu-id="d7768-118">As propriedades originais do autor permitem a preservação de informações de fora do domínio de mensagens local.</span><span class="sxs-lookup"><span data-stu-id="d7768-118">The original author properties allow for preservation of information from outside the local messaging domain.</span></span> <span data-ttu-id="d7768-119">Quando uma mensagem chega de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não são perdidas.</span><span class="sxs-lookup"><span data-stu-id="d7768-119">When a message arrives from another messaging domain, such as from the Internet, these properties provide a way to ensure that original information is not lost.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d7768-120">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d7768-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="d7768-121">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="d7768-121">Header files</span></span>

<span data-ttu-id="d7768-122">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d7768-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="d7768-123">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d7768-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="d7768-124">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d7768-124">Mapitags.h</span></span>
  
> <span data-ttu-id="d7768-125">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="d7768-125">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d7768-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7768-126">See also</span></span>



[<span data-ttu-id="d7768-127">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d7768-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d7768-128">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="d7768-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d7768-129">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d7768-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d7768-130">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d7768-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

