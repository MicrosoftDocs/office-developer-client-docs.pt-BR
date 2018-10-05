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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383622"
---
# <a name="pidtagconversationindex-canonical-property"></a><span data-ttu-id="d25f9-103">Propriedade canônica PidTagConversationIndex</span><span class="sxs-lookup"><span data-stu-id="d25f9-103">PidTagConversationIndex Canonical Property</span></span>

  
  
<span data-ttu-id="d25f9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d25f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d25f9-105">Contém um valor binário que indica a posição relativa desta mensagem dentro de um thread de conversação.</span><span class="sxs-lookup"><span data-stu-id="d25f9-105">Contains a binary value that indicates the relative position of this message within a conversation thread.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d25f9-106">Propriedades associadas:</span><span class="sxs-lookup"><span data-stu-id="d25f9-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d25f9-107">PR_CONVERSATION_INDEX</span><span class="sxs-lookup"><span data-stu-id="d25f9-107">PR_CONVERSATION_INDEX</span></span>  <br/> |
|<span data-ttu-id="d25f9-108">Identificador:</span><span class="sxs-lookup"><span data-stu-id="d25f9-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d25f9-109">0x0071</span><span class="sxs-lookup"><span data-stu-id="d25f9-109">0x0071</span></span>  <br/> |
|<span data-ttu-id="d25f9-110">Tipo de dados:</span><span class="sxs-lookup"><span data-stu-id="d25f9-110">Data type:</span></span>  <br/> |<span data-ttu-id="d25f9-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="d25f9-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="d25f9-112">Área:</span><span class="sxs-lookup"><span data-stu-id="d25f9-112">Area:</span></span>  <br/> |<span data-ttu-id="d25f9-113">Soluções gerais de mensagens</span><span class="sxs-lookup"><span data-stu-id="d25f9-113">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d25f9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="d25f9-114">Remarks</span></span>

<span data-ttu-id="d25f9-115">Um thread de conversação representa uma série de mensagens e respostas.</span><span class="sxs-lookup"><span data-stu-id="d25f9-115">A conversation thread represents a series of messages and replies.</span></span> <span data-ttu-id="d25f9-116">Essa propriedade normalmente é implementada usando valores de carimbo de data / hora concatenada.</span><span class="sxs-lookup"><span data-stu-id="d25f9-116">This property is usually implemented using concatenated time stamp values.</span></span> <span data-ttu-id="d25f9-117">Seu uso é opcional, mesmo se **PR_CONVERSATION_TOPIC** ([Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) estiver definida.</span><span class="sxs-lookup"><span data-stu-id="d25f9-117">Its use is optional, even if **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) is set.</span></span> 
  
<span data-ttu-id="d25f9-118">MAPI fornece a função [ScCreateConversationIndex](sccreateconversationindex.md) para criar ou atualizar um índice de conversa.</span><span class="sxs-lookup"><span data-stu-id="d25f9-118">MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index.</span></span> <span data-ttu-id="d25f9-119">A função usa o valor de índice atual como uma matriz de bytes contada e retornará o valor de índice com um carimbo de hora concatenado no final.</span><span class="sxs-lookup"><span data-stu-id="d25f9-119">The function takes the current index value as a counted byte array and returns the index value with a time stamp concatenated onto the end.</span></span> <span data-ttu-id="d25f9-120">Uma mensagem que representa uma resposta a outra mensagem deve usar **ScCreateConversationIndex** para atualizar esta propriedade.</span><span class="sxs-lookup"><span data-stu-id="d25f9-120">A message representing a reply to another message should use **ScCreateConversationIndex** to update this property.</span></span> 
  
<span data-ttu-id="d25f9-121">Um provedor de armazenamento de mensagem tem a opção de assegurar que **PR_CONVERSATION_INDEX** é sempre definida em mensagens de entrada ou saídas.</span><span class="sxs-lookup"><span data-stu-id="d25f9-121">A message store provider has the option of assuring that **PR_CONVERSATION_INDEX** is always set on incoming or outgoing messages.</span></span> <span data-ttu-id="d25f9-122">Ele pode fazer isso chamando **ScCreateConversationIndex**, com o valor existente, se essa propriedade estiver definida ou NULL se não estiver.</span><span class="sxs-lookup"><span data-stu-id="d25f9-122">It can do this by calling **ScCreateConversationIndex**, either with the existing value if this property is set or with NULL if it is not.</span></span> <span data-ttu-id="d25f9-123">Essa ação deve ser executada antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado.</span><span class="sxs-lookup"><span data-stu-id="d25f9-123">This action should be taken before [IMAPIProp::SaveChanges](imapiprop-savechanges.md) is called.</span></span> 
  
<span data-ttu-id="d25f9-124">Todas as mensagens que têm o mesmo valor para **PR_CONVERSATION_TOPIC** podem ser classificadas nessa propriedade para revelar a relação hierárquica das mensagens.</span><span class="sxs-lookup"><span data-stu-id="d25f9-124">All messages that have the same value for **PR_CONVERSATION_TOPIC** can be sorted on this property to reveal the hierarchical relationship of the messages.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="d25f9-125">Recursos relacionados</span><span class="sxs-lookup"><span data-stu-id="d25f9-125">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d25f9-126">Especificações de protocolo</span><span class="sxs-lookup"><span data-stu-id="d25f9-126">Protocol specifications</span></span>

<span data-ttu-id="d25f9-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d25f9-127">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d25f9-128">Fornece referências a relacionados especificações de protocolo do Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="d25f9-128">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d25f9-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d25f9-129">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d25f9-130">Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.</span><span class="sxs-lookup"><span data-stu-id="d25f9-130">Specifies the properties and operations that are permissible on email message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d25f9-131">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d25f9-131">Header files</span></span>

<span data-ttu-id="d25f9-132">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="d25f9-132">Mapidefs.h</span></span>
  
> <span data-ttu-id="d25f9-133">Fornece definições de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="d25f9-133">Provides data type definitions.</span></span>
    
<span data-ttu-id="d25f9-134">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="d25f9-134">Mapitags.h</span></span>
  
> <span data-ttu-id="d25f9-135">Contém definições das propriedades listadas como nomes alternativos.</span><span class="sxs-lookup"><span data-stu-id="d25f9-135">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d25f9-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="d25f9-136">See also</span></span>



[<span data-ttu-id="d25f9-137">Propriedades MAPI</span><span class="sxs-lookup"><span data-stu-id="d25f9-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d25f9-138">Propriedades MAPI canônicas</span><span class="sxs-lookup"><span data-stu-id="d25f9-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d25f9-139">Mapear nomes de propriedades canônicas para nomes MAPI</span><span class="sxs-lookup"><span data-stu-id="d25f9-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d25f9-140">Mapear nomes MAPI para nomes de propriedades canônicas</span><span class="sxs-lookup"><span data-stu-id="d25f9-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

