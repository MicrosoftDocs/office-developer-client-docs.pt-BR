---
title: IMessageGetAttachmentTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetAttachmentTable
api_type:
- COM
ms.assetid: e568917e-6085-4094-8728-89ba90a78c40
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 275dc17a141f1c002f62a43824174458e591d4de
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767381"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="8081c-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="8081c-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="8081c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8081c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8081c-105">Retorna a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8081c-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8081c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8081c-106">Parameters</span></span>

 <span data-ttu-id="8081c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8081c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8081c-108">[in] Bitmask dos sinalizadores que se relacionam com a criação da tabela.</span><span class="sxs-lookup"><span data-stu-id="8081c-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="8081c-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="8081c-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="8081c-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="8081c-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="8081c-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8081c-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="8081c-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="8081c-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="8081c-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="8081c-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="8081c-114">Permite que **GetAttachmentTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="8081c-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="8081c-115">Se a tabela não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="8081c-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="8081c-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8081c-116">_lppTable_</span></span>
  
> <span data-ttu-id="8081c-117">[out] Ponteiro para um ponteiro para a tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="8081c-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8081c-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8081c-118">Return value</span></span>

<span data-ttu-id="8081c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="8081c-119">S_OK</span></span> 
  
> <span data-ttu-id="8081c-120">A tabela de anexo foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="8081c-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8081c-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="8081c-121">Remarks</span></span>

<span data-ttu-id="8081c-122">O método **IMessage::GetAttachmentTable** retorna um ponteiro para a tabela de anexos da mensagem, que inclui informações sobre todos os anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="8081c-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="8081c-123">Os clientes podem obter acesso a um anexo através de apenas a tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="8081c-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="8081c-124">Recuperando o número de um anexo sua propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) um cliente pode usar vários métodos **IMessage** para trabalhar com o anexo.</span><span class="sxs-lookup"><span data-stu-id="8081c-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="8081c-125">Não há uma linha para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="8081c-125">There is one row for each attachment.</span></span> <span data-ttu-id="8081c-126">Para obter uma lista completa das colunas em uma tabela de anexo, consulte [As tabelas de anexo](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8081c-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="8081c-127">Um anexo normalmente não aparecem na tabela anexo até que o anexo e a mensagem foram salvos com uma chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="8081c-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="8081c-128">Tabelas do anexo são dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="8081c-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="8081c-129">Se um cliente cria um novo anexo, exclui um anexo existente ou altera um ou mais propriedades depois que as chamadas **SaveChanges** foram feitas no anexo na mensagem, a tabela de anexo será atualizada para refletir as novas informações.</span><span class="sxs-lookup"><span data-stu-id="8081c-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="8081c-130">Suportam a uma ampla variedade de restrições; algumas tabelas de anexo outros não.</span><span class="sxs-lookup"><span data-stu-id="8081c-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="8081c-131">Suporte a restrições depende da implementação do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8081c-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="8081c-132">Quando aberto inicialmente, tabelas de anexo não são necessariamente classificadas em alguma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="8081c-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="8081c-133">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta as seguintes chamadas à tabela de anexo:</span><span class="sxs-lookup"><span data-stu-id="8081c-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="8081c-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="8081c-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="8081c-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="8081c-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="8081c-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="8081c-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="8081c-137">Definindo as solicitações de sinalizador Unicode que as informações de quaisquer colunas de cadeia de caracteres retornada dessas chamadas estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="8081c-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="8081c-138">No entanto, porque nem todos os provedores de armazenamento de mensagem oferecem suporte a Unicode, defina esse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="8081c-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8081c-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="8081c-139">See also</span></span>



[<span data-ttu-id="8081c-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="8081c-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="8081c-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="8081c-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="8081c-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="8081c-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="8081c-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="8081c-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

