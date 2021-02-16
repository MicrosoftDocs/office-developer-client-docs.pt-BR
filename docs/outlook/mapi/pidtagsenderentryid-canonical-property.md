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
ms.openlocfilehash: 0bc8b8bd76d553cc4e12e331e9fe7047ef7aaf4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358909"
---
# <a name="pidtagsenderentryid-canonical-property"></a><span data-ttu-id="8bb53-103">Propriedade canônica PidTagSenderEntryId</span><span class="sxs-lookup"><span data-stu-id="8bb53-103">PidTagSenderEntryId Canonical Property</span></span>

  
  
<span data-ttu-id="8bb53-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8bb53-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8bb53-105">Contém o identificador de entrada do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8bb53-105">Contains the message sender's entry identifier.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8bb53-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="8bb53-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8bb53-107">PR_SENDER_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="8bb53-107">PR_SENDER_ENTRYID</span></span>  <br/> |
|<span data-ttu-id="8bb53-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="8bb53-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8bb53-109">0x0C19</span><span class="sxs-lookup"><span data-stu-id="8bb53-109">0x0C19</span></span>  <br/> |
|<span data-ttu-id="8bb53-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="8bb53-110">Data type:</span></span>  <br/> |<span data-ttu-id="8bb53-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="8bb53-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="8bb53-112">Área:</span><span class="sxs-lookup"><span data-stu-id="8bb53-112">Area:</span></span>  <br/> |<span data-ttu-id="8bb53-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="8bb53-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8bb53-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bb53-114">Remarks</span></span>

<span data-ttu-id="8bb53-115">Essa propriedade é uma das propriedades de endereço do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8bb53-115">This property is one of the address properties for the message sender.</span></span> <span data-ttu-id="8bb53-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar valores existentes anteriormente.</span><span class="sxs-lookup"><span data-stu-id="8bb53-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="8bb53-117">Se nenhum provedor de transporte tiver fornecido qualquer propriedade de endereço do remetente, o spooler MAPI tentará preenchê-las chamando o método [IMAPISession::QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="8bb53-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="8bb53-118">Se nenhum identificador de entrada tiver sido fornecido, o spooler MAPI um identificador correspondente à cadeia de caracteres "Unknown" nesta propriedade.</span><span class="sxs-lookup"><span data-stu-id="8bb53-118">If no entry identifiers have been provided, the MAPI spooler an identifier corresponding to the string "Unknown" in this property.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="8bb53-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bb53-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8bb53-120">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="8bb53-120">Protocol specifications</span></span>

<span data-ttu-id="8bb53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-122">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="8bb53-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8bb53-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-124">Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="8bb53-124">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="8bb53-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-126">Especifica as propriedades e operações que representam itens RSS.</span><span class="sxs-lookup"><span data-stu-id="8bb53-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="8bb53-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-128">Lida com a ordem e o fluxo para transferências de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="8bb53-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="8bb53-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-130">Converte entre IETF RFC2445, RFC2446 e RFC2447 e objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="8bb53-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="8bb53-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-131">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-132">Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.</span><span class="sxs-lookup"><span data-stu-id="8bb53-132">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8bb53-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8bb53-133">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8bb53-134">Especifica as propriedades e operações que são permitidas para postagem de objetos.</span><span class="sxs-lookup"><span data-stu-id="8bb53-134">Specifies the properties and operations that are permissible for post objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8bb53-135">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="8bb53-135">Header files</span></span>

<span data-ttu-id="8bb53-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8bb53-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="8bb53-137">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="8bb53-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="8bb53-138">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="8bb53-138">Mapitags.h</span></span>
  
> <span data-ttu-id="8bb53-139">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="8bb53-139">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8bb53-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="8bb53-140">See also</span></span>



[<span data-ttu-id="8bb53-141">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="8bb53-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8bb53-142">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="8bb53-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8bb53-143">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="8bb53-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8bb53-144">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="8bb53-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

