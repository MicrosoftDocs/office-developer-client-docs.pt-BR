---
title: Propriedade canônica PidTagSenderEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderEntryId
api_type:
- COM
ms.assetid: 9f311dd2-853e-46f7-966a-c2ab7a1fb6c5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 46ccc3c7e07e6920508fea630c96700d39366a35
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770011"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="89820-103">Propriedade canônica PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="89820-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="89820-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="89820-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="89820-105">Contém o identificador de entrada do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="89820-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89820-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="89820-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="89820-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="89820-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="89820-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="89820-108">Identifier:</span></span>  <br/> |<span data-ttu-id="89820-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="89820-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="89820-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="89820-110">Data type:</span></span>  <br/> |<span data-ttu-id="89820-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="89820-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="89820-112">Área:</span><span class="sxs-lookup"><span data-stu-id="89820-112">Area:</span></span>  <br/> |<span data-ttu-id="89820-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="89820-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89820-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="89820-114">Remarks</span></span>

<span data-ttu-id="89820-115">Essa propriedade é uma das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="89820-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="89820-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar quaisquer valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="89820-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="89820-117">Se nenhum provedor de transporte tem fornecido quaisquer propriedades de endereço do remetente, o MAPI spooler tenta preencher chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="89820-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="89820-118">Se nenhuma entrada identificadores foram fornecidos, o MAPI spooler um identificador correspondente à cadeia de caracteres "Desconhecido" nessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="89820-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="89820-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="89820-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="89820-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="89820-120">Protocol specifications</span></span>

<span data-ttu-id="89820-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-122">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="89820-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="89820-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-123">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="89820-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="89820-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-125">[[MS-OXORSS]](http://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-126">Especifica as propriedades e operações que representam os itens RSS.</span><span class="sxs-lookup"><span data-stu-id="89820-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="89820-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-127">[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-128">Trata da ordem e o fluxo para transferências de dados entre um cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="89820-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="89820-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-129">[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-130">Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.</span><span class="sxs-lookup"><span data-stu-id="89820-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="89820-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-131">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-132">Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.</span><span class="sxs-lookup"><span data-stu-id="89820-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="89820-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="89820-133">[[MS-OXOPOST]](http://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="89820-134">Especifica as propriedades e operações que são permitidas para postagem objetos.</span><span class="sxs-lookup"><span data-stu-id="89820-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="89820-135">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="89820-135">Header files</span></span>

<span data-ttu-id="89820-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="89820-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="89820-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="89820-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="89820-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="89820-138">Mapitags.h</span></span>
  
> <span data-ttu-id="89820-139">Contém definições das propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="89820-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="89820-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="89820-140">See also</span></span>



[<span data-ttu-id="89820-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="89820-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="89820-142">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="89820-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="89820-143">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="89820-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="89820-144">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="89820-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

