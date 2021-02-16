---
title: Propriedade canônica PidTagMessageAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageAttachments
api_type:
- HeaderDef
ms.assetid: 85762771-b823-4227-9a7b-75b6ac280b2d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 975f52e6ea0ca7a469a027565f845f9dc0f9c2cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342563"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="02b43-103">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="02b43-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="02b43-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="02b43-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="02b43-105">Contém uma tabela de anexos de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="02b43-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="02b43-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="02b43-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="02b43-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="02b43-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="02b43-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="02b43-108">Identifier:</span></span>  <br/> |<span data-ttu-id="02b43-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="02b43-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="02b43-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="02b43-110">Data type:</span></span>  <br/> |<span data-ttu-id="02b43-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="02b43-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="02b43-112">Área:</span><span class="sxs-lookup"><span data-stu-id="02b43-112">Area:</span></span>  <br/> |<span data-ttu-id="02b43-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="02b43-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02b43-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02b43-114">Remarks</span></span>

<span data-ttu-id="02b43-115">Essa propriedade pode ser excluída nas [operações IMAPIProp::CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp::CopyProps.](imapiprop-copyprops.md)</span><span class="sxs-lookup"><span data-stu-id="02b43-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="02b43-116">Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo [método IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="02b43-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="02b43-117">Seu conteúdo deve ser acessado pelo [método IMAPIProp::OpenProperty,](imapiprop-openproperty.md) solicitando o **identificador IID_IMAPITable** interface.</span><span class="sxs-lookup"><span data-stu-id="02b43-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="02b43-118">Os provedores de serviços devem reportá-lo ao método [IMAPIProp::GetPropList](imapiprop-getproplist.md) se ele estiver definido, mas, opcionalmente, pode relaí-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="02b43-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="02b43-119">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o [método IMessage::GetAttachmentTable.](imessage-getattachmenttable.md)</span><span class="sxs-lookup"><span data-stu-id="02b43-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="02b43-120">Para obter mais informações, consulte [Attachment Tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="02b43-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="02b43-121">Essa propriedade pode ser usada para restrição de subobjeto especificando-a na [estrutura SSubRestriction.](ssubrestriction.md)</span><span class="sxs-lookup"><span data-stu-id="02b43-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="02b43-122">Isso permite que o cliente limite a exibição de um contêiner a mensagens com anexos que atenderem a determinados critérios.</span><span class="sxs-lookup"><span data-stu-id="02b43-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="02b43-123">Uma mensagem se qualifica para exibição se pelo menos uma linha em sua tabela de anexos, ou seja, um anexo, satisfaz a restrição de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="02b43-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="02b43-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="02b43-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="02b43-125">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="02b43-125">Protocol specifications</span></span>

<span data-ttu-id="02b43-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02b43-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02b43-127">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="02b43-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="02b43-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02b43-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02b43-129">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="02b43-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="02b43-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="02b43-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="02b43-131">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="02b43-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="02b43-132">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="02b43-132">Header files</span></span>

<span data-ttu-id="02b43-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="02b43-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="02b43-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="02b43-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="02b43-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="02b43-135">Mapitags.h</span></span>
  
> <span data-ttu-id="02b43-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="02b43-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="02b43-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="02b43-137">See also</span></span>



[<span data-ttu-id="02b43-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="02b43-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="02b43-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="02b43-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="02b43-140">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="02b43-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="02b43-141">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="02b43-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

