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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9a77d335f3c8980de29dab6e14079c83bd711b43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421169"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="6cf0f-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="6cf0f-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="6cf0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6cf0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6cf0f-105">Retorna a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6cf0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cf0f-106">Parameters</span></span>

 <span data-ttu-id="6cf0f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6cf0f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6cf0f-108">[in] Bitmask de sinalizadores relacionados à criação da tabela.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="6cf0f-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="6cf0f-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="6cf0f-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6cf0f-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6cf0f-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="6cf0f-112">Se o MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres estão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="6cf0f-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="6cf0f-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="6cf0f-114">Permite que **GetAttachmentTable** retorne com êxito, possivelmente antes da tabela estar totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="6cf0f-115">Se a tabela não estiver disponível, fazer uma chamada subsequente pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="6cf0f-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6cf0f-116">_lppTable_</span></span>
  
> <span data-ttu-id="6cf0f-117">[out] Ponteiro para um ponteiro para a tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6cf0f-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6cf0f-118">Return value</span></span>

<span data-ttu-id="6cf0f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="6cf0f-119">S_OK</span></span> 
  
> <span data-ttu-id="6cf0f-120">A tabela de anexos foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6cf0f-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cf0f-121">Remarks</span></span>

<span data-ttu-id="6cf0f-122">O **método IMessage::GetAttachmentTable** retorna um ponteiro para a tabela de anexos da mensagem, que inclui informações sobre todos os anexos na mensagem.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="6cf0f-123">Os clientes só podem obter acesso a um anexo por meio da tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="6cf0f-124">Ao recuperar o número de um anexo, sua propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) de um cliente pode usar vários dos métodos **IMessage** para trabalhar com o anexo.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="6cf0f-125">Há uma linha para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-125">There is one row for each attachment.</span></span> <span data-ttu-id="6cf0f-126">Para uma lista completa das colunas em uma tabela de anexos, consulte [Attachment Tables](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="6cf0f-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="6cf0f-127">Um anexo geralmente não aparece na tabela de anexos até que o anexo e a mensagem tenham sido salvos com uma chamada para [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="6cf0f-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="6cf0f-128">As tabelas de anexos são dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="6cf0f-129">Se um cliente cria um novo anexo, exclui um anexo existente ou altera uma ou mais propriedades depois que as chamadas **SaveChanges** são feitas no anexo na mensagem, a tabela de anexos será atualizada para refletir as novas informações.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="6cf0f-130">Algumas tabelas de anexos suportam uma ampla variedade de restrições; outras não fazem isso.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="6cf0f-131">O suporte para restrições depende da implementação do provedor do armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="6cf0f-132">Quando abertas inicialmente, as tabelas de anexos não são necessariamente ordenadas em uma ordem específica.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="6cf0f-133">A definição MAPI_UNICODE sinalizador de configuração no  _parâmetro ulFlags_ afeta as seguintes chamadas para a tabela de anexos:</span><span class="sxs-lookup"><span data-stu-id="6cf0f-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="6cf0f-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="6cf0f-135">[IMAPITable::QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="6cf0f-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="6cf0f-137">A configuração do sinalizador Unicode solicita que as informações de quaisquer colunas de cadeia de caracteres retornadas dessas chamadas sejam no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="6cf0f-138">No entanto, como nem todos os provedores de armazenamento de mensagens suportam Unicode, definir esse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="6cf0f-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6cf0f-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="6cf0f-139">See also</span></span>



[<span data-ttu-id="6cf0f-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="6cf0f-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="6cf0f-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="6cf0f-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="6cf0f-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="6cf0f-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="6cf0f-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="6cf0f-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

