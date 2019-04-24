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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349270"
---
# <a name="imessagegetattachmenttable"></a><span data-ttu-id="f01c9-103">IMessage::GetAttachmentTable</span><span class="sxs-lookup"><span data-stu-id="f01c9-103">IMessage::GetAttachmentTable</span></span>

  
  
<span data-ttu-id="f01c9-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f01c9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f01c9-105">Retorna a tabela de anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f01c9-105">Returns the message's attachment table.</span></span>
  
```cpp
HRESULT GetAttachmentTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="f01c9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f01c9-106">Parameters</span></span>

 <span data-ttu-id="f01c9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f01c9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f01c9-108">no Bitmask de sinalizadores relacionados à criação da tabela.</span><span class="sxs-lookup"><span data-stu-id="f01c9-108">[in] Bitmask of flags that relate to the creation of the table.</span></span> <span data-ttu-id="f01c9-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f01c9-109">The following flag can be set:</span></span> 
    
<span data-ttu-id="f01c9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f01c9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f01c9-111">As colunas de cadeia de caracteres estão no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f01c9-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="f01c9-112">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas da cadeia de caracteres estarão no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f01c9-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
<span data-ttu-id="f01c9-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="f01c9-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="f01c9-114">Permite \*\*\*\* que GetAttachmentTable seja retornado com êxito, possivelmente antes que a tabela esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="f01c9-114">Allows **GetAttachmentTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="f01c9-115">Se a tabela não estiver disponível, fazer uma chamada subsequente para ela pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="f01c9-115">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
 <span data-ttu-id="f01c9-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="f01c9-116">_lppTable_</span></span>
  
> <span data-ttu-id="f01c9-117">bota Ponteiro para um ponteiro para a tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="f01c9-117">[out] Pointer to a pointer to the attachment table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f01c9-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="f01c9-118">Return value</span></span>

<span data-ttu-id="f01c9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f01c9-119">S_OK</span></span> 
  
> <span data-ttu-id="f01c9-120">A tabela de anexos foi recuperada com êxito.</span><span class="sxs-lookup"><span data-stu-id="f01c9-120">The attachment table was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f01c9-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="f01c9-121">Remarks</span></span>

<span data-ttu-id="f01c9-122">O método **IMessage::** GetAttachmentTable retorna um ponteiro para a tabela de anexos da mensagem, que inclui informações sobre todos os anexos da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f01c9-122">The **IMessage::GetAttachmentTable** method returns a pointer to the message's attachment table, which includes information about all of the attachments in the message.</span></span> <span data-ttu-id="f01c9-123">Os clientes podem ter acesso a um anexo apenas por meio da tabela de anexos.</span><span class="sxs-lookup"><span data-stu-id="f01c9-123">Clients can get access to an attachment only through the attachment table.</span></span> <span data-ttu-id="f01c9-124">Ao recuperar o número de um anexo sua propriedade **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)), um cliente pode usar vários dos métodos **IMessage** para trabalhar com o anexo.</span><span class="sxs-lookup"><span data-stu-id="f01c9-124">By retrieving an attachment's number its **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property a client can use several of the **IMessage** methods to work with the attachment.</span></span> 
  
<span data-ttu-id="f01c9-125">Há uma linha para cada anexo.</span><span class="sxs-lookup"><span data-stu-id="f01c9-125">There is one row for each attachment.</span></span> <span data-ttu-id="f01c9-126">Para obter uma lista completa das colunas em uma tabela de anexos, consulte [tabelas de anexo](attachment-tables.md).</span><span class="sxs-lookup"><span data-stu-id="f01c9-126">For a complete list of the columns in an attachment table, see [Attachment Tables](attachment-tables.md).</span></span>
  
<span data-ttu-id="f01c9-127">Um anexo normalmente não aparece na tabela de anexos até que o anexo e a mensagem tenham sido salvos com uma chamada para [IMAPIProp:: SaveChanges](imapiprop-savechanges.md).</span><span class="sxs-lookup"><span data-stu-id="f01c9-127">An attachment usually does not appear in the attachment table until both the attachment and the message have been saved with a call to [IMAPIProp::SaveChanges](imapiprop-savechanges.md).</span></span> <span data-ttu-id="f01c9-128">As tabelas de anexo são dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="f01c9-128">Attachment tables are dynamic.</span></span> <span data-ttu-id="f01c9-129">Se um cliente criar um novo anexo, excluir um anexo existente ou alterar uma ou mais propriedades depois que as chamadas de **SaveChanges** forem feitas no anexo da mensagem, a tabela de anexos será atualizada para refletir as novas informações.</span><span class="sxs-lookup"><span data-stu-id="f01c9-129">If a client creates a new attachment, deletes an existing attachment, or changes one or more properties once the **SaveChanges** calls have been made on the attachment on the message, the attachment table will be updated to reflect the new information.</span></span> 
  
<span data-ttu-id="f01c9-130">Algumas tabelas de anexo dão suporte a uma ampla variedade de restrições; outros não.</span><span class="sxs-lookup"><span data-stu-id="f01c9-130">Some attachment tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="f01c9-131">O suporte para restrições depende da implementação do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="f01c9-131">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="f01c9-132">Quando aberto inicialmente, as tabelas de anexos não são necessariamente classificadas em qualquer ordem específica.</span><span class="sxs-lookup"><span data-stu-id="f01c9-132">When initially opened, attachment tables are not necessarily sorted in any particular order.</span></span> 
  
<span data-ttu-id="f01c9-133">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta as seguintes chamadas para a tabela de anexos:</span><span class="sxs-lookup"><span data-stu-id="f01c9-133">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the attachment table:</span></span> 
  
- <span data-ttu-id="f01c9-134">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="f01c9-134">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="f01c9-135">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="f01c9-135">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="f01c9-136">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="f01c9-136">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="f01c9-137">Definir o sinalizador Unicode solicita que as informações de qualquer coluna de cadeia de caracteres retornada dessas chamadas estejam no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f01c9-137">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="f01c9-138">No enTanto, como nem todos os provedores de repositórios de mensagens dão suporte a Unicode, a configuração desse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="f01c9-138">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f01c9-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="f01c9-139">See also</span></span>



[<span data-ttu-id="f01c9-140">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="f01c9-140">IMessage::CreateAttach</span></span>](imessage-createattach.md)
  
[<span data-ttu-id="f01c9-141">IMessage::DeleteAttach</span><span class="sxs-lookup"><span data-stu-id="f01c9-141">IMessage::DeleteAttach</span></span>](imessage-deleteattach.md)
  
[<span data-ttu-id="f01c9-142">IMessage::OpenAttach</span><span class="sxs-lookup"><span data-stu-id="f01c9-142">IMessage::OpenAttach</span></span>](imessage-openattach.md)
  
[<span data-ttu-id="f01c9-143">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f01c9-143">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

