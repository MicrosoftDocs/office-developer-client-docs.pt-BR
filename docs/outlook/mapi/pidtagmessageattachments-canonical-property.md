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
ms.sourcegitcommit: 43cff5789e0a0a8cda11277c1a636c8b32d28cdb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/06/2019
ms.locfileid: "30413970"
---
# <a name="pidtagmessageattachments-canonical-property"></a><span data-ttu-id="38ee2-103">Propriedade canônica PidTagMessageAttachments</span><span class="sxs-lookup"><span data-stu-id="38ee2-103">PidTagMessageAttachments Canonical Property</span></span>

  
  
<span data-ttu-id="38ee2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="38ee2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="38ee2-105">Contém uma tabela de anexos para uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="38ee2-105">Contains a table of attachments for a message.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38ee2-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="38ee2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="38ee2-107">PR_MESSAGE_ATTACHMENTS</span><span class="sxs-lookup"><span data-stu-id="38ee2-107">PR_MESSAGE_ATTACHMENTS</span></span>  <br/> |
|<span data-ttu-id="38ee2-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="38ee2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="38ee2-109">0x0E13</span><span class="sxs-lookup"><span data-stu-id="38ee2-109">0x0E13</span></span>  <br/> |
|<span data-ttu-id="38ee2-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="38ee2-110">Data type:</span></span>  <br/> |<span data-ttu-id="38ee2-111">PT_OBJECT</span><span class="sxs-lookup"><span data-stu-id="38ee2-111">PT_OBJECT</span></span>  <br/> |
|<span data-ttu-id="38ee2-112">Área:</span><span class="sxs-lookup"><span data-stu-id="38ee2-112">Area:</span></span>  <br/> |<span data-ttu-id="38ee2-113">Anexo de mensagem</span><span class="sxs-lookup"><span data-stu-id="38ee2-113">Message attachment</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38ee2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38ee2-114">Remarks</span></span>

<span data-ttu-id="38ee2-115">Esta propriedade pode ser excluída nas operações de [IMAPIProp:: CopyTo](imapiprop-copyto.md) ou incluída nas operações [IMAPIProp:: CopyProps](imapiprop-copyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="38ee2-115">This property can be excluded in [IMAPIProp::CopyTo](imapiprop-copyto.md) operations or included in [IMAPIProp::CopyProps](imapiprop-copyprops.md) operations.</span></span> <span data-ttu-id="38ee2-116">Como uma propriedade do tipo PT_OBJECT, ela não pode ser recuperada com êxito pelo método [IMAPIProp::](imapiprop-getprops.md) GetProps.</span><span class="sxs-lookup"><span data-stu-id="38ee2-116">As a property of type PT_OBJECT, it cannot be successfully retrieved by the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> <span data-ttu-id="38ee2-117">Seu conteúdo deve ser acessado pelo método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) , solicitando o identificador de interface **IID_IMAPITable** .</span><span class="sxs-lookup"><span data-stu-id="38ee2-117">Its contents should be accessed by the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method, requesting the **IID_IMAPITable** interface identifier.</span></span> <span data-ttu-id="38ee2-118">Os provedores de serviços devem relatá-lo para o método [IMAPIProp::](imapiprop-getproplist.md) getproplist, se estiver definido, mas pode opcionalmente relatá-lo ou não se ele não estiver definido.</span><span class="sxs-lookup"><span data-stu-id="38ee2-118">Service providers must report it to the [IMAPIProp::GetPropList](imapiprop-getproplist.md) method if it is set, but may optionally report it or not if it is not set.</span></span> 
  
<span data-ttu-id="38ee2-119">Para recuperar o conteúdo da tabela, um aplicativo cliente deve chamar o método [IMessage::](imessage-getattachmenttable.md) GetAttachmentTable.</span><span class="sxs-lookup"><span data-stu-id="38ee2-119">To retrieve table contents, a client application should call the [IMessage::GetAttachmentTable](imessage-getattachmenttable.md) method.</span></span> <span data-ttu-id="38ee2-120">Para obter mais informações, consulte [tabelas de anexo](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="38ee2-120">For more information, see [Attachment Tables](attachment-tables.md).</span></span> 
  
<span data-ttu-id="38ee2-121">Essa propriedade pode ser usada para restrição de subobjeto especificando-a na estrutura [SSubRestriction](ssubrestriction.md) .</span><span class="sxs-lookup"><span data-stu-id="38ee2-121">This property can be used for subobject restriction by specifying it in the [SSubRestriction](ssubrestriction.md) structure.</span></span> <span data-ttu-id="38ee2-122">Isso permite que o cliente limite o modo de exibição de um contêiner às mensagens com anexos que atendam aos critérios fornecidos.</span><span class="sxs-lookup"><span data-stu-id="38ee2-122">This allows the client to limit the view of a container to messages with attachments meeting given criteria.</span></span> <span data-ttu-id="38ee2-123">Uma mensagem é qualificada para exibir se pelo menos uma linha na tabela de anexos, ou seja, um anexo, satisfizer a restrição de subobjeto.</span><span class="sxs-lookup"><span data-stu-id="38ee2-123">A message qualifies for viewing if at least one row in its attachments table, that is, one attachment, satisfies the subobject restriction.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="38ee2-124">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="38ee2-124">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="38ee2-125">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="38ee2-125">Protocol specifications</span></span>

<span data-ttu-id="38ee2-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ee2-126">[[MS-OXCDATA]](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ee2-127">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="38ee2-127">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="38ee2-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ee2-128">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ee2-129">Define as estruturas de dados básicas que são usadas em operações remotas.</span><span class="sxs-lookup"><span data-stu-id="38ee2-129">Defines the basic data structures that are used in remote operations.</span></span>
    
<span data-ttu-id="38ee2-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="38ee2-130">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="38ee2-131">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="38ee2-131">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="38ee2-132">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="38ee2-132">Header files</span></span>

<span data-ttu-id="38ee2-133">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="38ee2-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="38ee2-134">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="38ee2-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="38ee2-135">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="38ee2-135">Mapitags.h</span></span>
  
> <span data-ttu-id="38ee2-136">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="38ee2-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="38ee2-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="38ee2-137">See also</span></span>



[<span data-ttu-id="38ee2-138">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="38ee2-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="38ee2-139">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="38ee2-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="38ee2-140">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="38ee2-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="38ee2-141">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="38ee2-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

