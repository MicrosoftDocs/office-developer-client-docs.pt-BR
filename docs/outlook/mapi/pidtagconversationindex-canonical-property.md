---
title: Propriedade canônica PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334717"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="18765-103">Propriedade canônica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="18765-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="18765-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18765-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18765-105">Contém um valor binário que indica a posição relativa dessa mensagem em um thread de conversa.</span><span class="sxs-lookup"><span data-stu-id="18765-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18765-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="18765-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="18765-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="18765-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="18765-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="18765-108">Identifier:</span></span>  <br/> |<span data-ttu-id="18765-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="18765-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="18765-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="18765-110">Data type:</span></span>  <br/> |<span data-ttu-id="18765-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="18765-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="18765-112">Área:</span><span class="sxs-lookup"><span data-stu-id="18765-112">Area:</span></span>  <br/> |<span data-ttu-id="18765-113">Envio de mensagens gerais</span><span class="sxs-lookup"><span data-stu-id="18765-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18765-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="18765-114">Remarks</span></span>

<span data-ttu-id="18765-115">Um thread de conversa representa uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="18765-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="18765-116">Essa propriedade geralmente é implementada usando valores de carimbo de data/hora concatenados.</span><span class="sxs-lookup"><span data-stu-id="18765-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="18765-117">Seu uso é opcional, mesmo que **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) seja definido.</span><span class="sxs-lookup"><span data-stu-id="18765-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="18765-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span><span class="sxs-lookup"><span data-stu-id="18765-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="18765-119">A função assume o valor de índice atual como uma matriz de byte contada e retorna o valor de índice com um carimbo de data/hora concatenado até o final.</span><span class="sxs-lookup"><span data-stu-id="18765-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="18765-120">Uma mensagem que representa uma resposta a outra mensagem deve usar **ScCreateConversationIndex** para atualizar essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="18765-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="18765-121">Um provedor de armazenamento de mensagens tem a opção de PR_CONVERSATION_INDEX **está** sempre definida em mensagens de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="18765-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="18765-122">Isso pode ser feito chamando **ScCreateConversationIndex**, com o valor existente se essa propriedade estiver definida ou com NULL se não estiver.</span><span class="sxs-lookup"><span data-stu-id="18765-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="18765-123">Essa ação deve ser realizada antes [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="18765-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="18765-124">Todas as mensagens que tenham o mesmo valor **para PR_CONVERSATION_TOPIC** podem ser ordenadas nessa propriedade para revelar a relação hierárquica das mensagens.</span><span class="sxs-lookup"><span data-stu-id="18765-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="18765-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="18765-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="18765-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="18765-126">Protocol specifications</span></span>

<span data-ttu-id="18765-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18765-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18765-128">Fornece referências a especificações de protocolo relacionadas do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="18765-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="18765-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="18765-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="18765-130">Especifica as propriedades e operações permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="18765-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="18765-131">Arquivos de header</span><span class="sxs-lookup"><span data-stu-id="18765-131">Header files</span></span>

<span data-ttu-id="18765-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="18765-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="18765-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="18765-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="18765-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="18765-134">Mapitags.h</span></span>
  
> <span data-ttu-id="18765-135">Contém definições de propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="18765-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="18765-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="18765-136">See also</span></span>



[<span data-ttu-id="18765-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="18765-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="18765-138">Propriedades canônicas MAPI</span><span class="sxs-lookup"><span data-stu-id="18765-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="18765-139">Mapeando nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="18765-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="18765-140">Mapeando nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="18765-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

