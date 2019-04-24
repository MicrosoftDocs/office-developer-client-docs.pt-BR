---
title: Propriedade canônica PidTagSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSenderName
api_type:
- COM
ms.assetid: 33fb53a8-4c7b-4418-8849-b6f9a1580172
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 953e792b6d18f7da9ee7eb17e07e6e05557e98ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355066"
---
# <a name="pidtagsendername-canonical-property"></a><span data-ttu-id="e8b2f-103">Propriedade canônica PidTagSenderName</span><span class="sxs-lookup"><span data-stu-id="e8b2f-103">PidTagSenderName Canonical Property</span></span>

  
  
<span data-ttu-id="e8b2f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8b2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8b2f-105">Contém o nome de exibição do remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-105">Contains the message sender's display name.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8b2f-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="e8b2f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e8b2f-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span><span class="sxs-lookup"><span data-stu-id="e8b2f-107">PR_SENDER_NAME, PR_SENDER_NAME_A, PR_SENDER_NAME_W</span></span>  <br/> |
|<span data-ttu-id="e8b2f-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="e8b2f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e8b2f-109">0x0C1A</span><span class="sxs-lookup"><span data-stu-id="e8b2f-109">0x0C1A</span></span>  <br/> |
|<span data-ttu-id="e8b2f-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="e8b2f-110">Data type:</span></span>  <br/> |<span data-ttu-id="e8b2f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e8b2f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="e8b2f-112">Área:</span><span class="sxs-lookup"><span data-stu-id="e8b2f-112">Area:</span></span>  <br/> |<span data-ttu-id="e8b2f-113">Endereço</span><span class="sxs-lookup"><span data-stu-id="e8b2f-113">Address</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8b2f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8b2f-114">Remarks</span></span>

<span data-ttu-id="e8b2f-115">Essas propriedades são exemplos das propriedades de endereço para o remetente da mensagem.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-115">These properties are examples of the address properties for the message sender.</span></span> <span data-ttu-id="e8b2f-116">Ele deve ser definido pelo provedor de transporte de saída, que nunca deve propagar nenhum valor existente anteriormente.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-116">It must be set by the outgoing transport provider, which should never propagate any previously existing values.</span></span>
  
<span data-ttu-id="e8b2f-117">Se nenhum provedor de transporte tiver fornecido Propriedades de endereço de remetente, o spooler MAPI tentará preenchê-las chamando o método [IMAPISession:: QueryIdentity](imapisession-queryidentity.md) para um identificador de entrada.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-117">If no transport provider has supplied any sender address properties, the MAPI spooler attempts to fill them in by calling the [IMAPISession::QueryIdentity](imapisession-queryidentity.md) method for an entry identifier.</span></span> <span data-ttu-id="e8b2f-118">Se nenhum identificador de entrada tiver sido fornecido, o spooler MAPI armazena "Unknown" em todas as propriedades de endereço de remetente do tipo PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-118">If no entry identifiers have been provided, the MAPI spooler stores "Unknown" in all the sender address properties of type PT_TSTRING.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e8b2f-119">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="e8b2f-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e8b2f-120">Especificações do protocolo</span><span class="sxs-lookup"><span data-stu-id="e8b2f-120">Protocol specifications</span></span>

<span data-ttu-id="e8b2f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-121">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-122">Fornece referências às especificações relacionadas do protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e8b2f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-123">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-124">Descreve o formato das mensagens usadas para enviar informações relacionadas às pastas de compartilhamento no cliente.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-124">Describes the format of messages used to send information related to sharing folders on the client.</span></span>
    
<span data-ttu-id="e8b2f-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-125">[[MS-OXORSS]](https://msdn.microsoft.com/library/53bc9634-0040-4b5a-aecd-29781d826009%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-126">Especifica as propriedades e operações que representam itens RSS.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-126">Specifies the properties and operations that represent RSS items.</span></span>
    
<span data-ttu-id="e8b2f-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-127">[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-128">Lida com a ordem e o fluxo para transferência de dados entre um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-128">Handles the order and flow for data transfers between a client and server.</span></span>
    
<span data-ttu-id="e8b2f-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-129">[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-130">Converte entre o IETF RFC2445, o RFC2446 e o RFC2447 e os objetos de compromisso e reunião.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-130">Converts between IETF RFC2445, RFC2446, and RFC2447, and appointment and meeting objects.</span></span>
    
<span data-ttu-id="e8b2f-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-131">[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-132">Especifica as propriedades e as operações que são permitidas para objetos post.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-132">Specifies the properties and operations that are permissible for post objects.</span></span>
    
<span data-ttu-id="e8b2f-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-133">[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-134">Especifica as propriedades e as operações que são permitidas para contatos e listas de distribuição pessoal.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-134">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
<span data-ttu-id="e8b2f-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e8b2f-135">[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e8b2f-136">Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-136">Encodes and decodes message and attachment objects to an efficient stream representation.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e8b2f-137">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8b2f-137">Header files</span></span>

<span data-ttu-id="e8b2f-138">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="e8b2f-138">Mapidefs.h</span></span>
  
> <span data-ttu-id="e8b2f-139">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-139">Provides data type definitions.</span></span>
    
<span data-ttu-id="e8b2f-140">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="e8b2f-140">Mapitags.h</span></span>
  
> <span data-ttu-id="e8b2f-141">Contém definições de propriedades listadas como propriedades associadas.</span><span class="sxs-lookup"><span data-stu-id="e8b2f-141">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e8b2f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8b2f-142">See also</span></span>



[<span data-ttu-id="e8b2f-143">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b2f-143">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e8b2f-144">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b2f-144">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e8b2f-145">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="e8b2f-145">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e8b2f-146">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="e8b2f-146">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

