---
title: IMessageGetRecipientTable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMessage.GetRecipientTable
api_type:
- COM
ms.assetid: a335dfca-44da-452e-b16f-25d314b1758f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5908069f5fa887fd9d2e3f8c0df75f2e3d69515c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579533"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="791ac-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="791ac-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="791ac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="791ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="791ac-105">Retorna a tabela de destinatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="791ac-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="791ac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="791ac-106">Parameters</span></span>

 <span data-ttu-id="791ac-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="791ac-107">_ulFlags_</span></span>
  
> <span data-ttu-id="791ac-108">[in] Bitmask dos sinalizadores que controla o retorno da tabela.</span><span class="sxs-lookup"><span data-stu-id="791ac-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="791ac-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="791ac-109">The following flags can be set:</span></span>
    
<span data-ttu-id="791ac-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="791ac-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="791ac-111">Permite que **GetRecipientTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="791ac-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="791ac-112">Se a tabela não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="791ac-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="791ac-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="791ac-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="791ac-114">Colunas de cadeia de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="791ac-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="791ac-115">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="791ac-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="791ac-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="791ac-116">_lppTable_</span></span>
  
> <span data-ttu-id="791ac-117">[out] Ponteiro para um ponteiro para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="791ac-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="791ac-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="791ac-118">Return value</span></span>

<span data-ttu-id="791ac-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="791ac-119">S_OK</span></span> 
  
> <span data-ttu-id="791ac-120">A tabela de destinatários foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="791ac-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="791ac-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="791ac-121">Remarks</span></span>

<span data-ttu-id="791ac-122">O método **IMessage::GetRecipientTable** retorna um ponteiro para a tabela de destinatário da mensagem, que inclui informações sobre todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="791ac-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="791ac-123">Não há uma linha para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="791ac-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="791ac-124">Tabelas de destinatários têm outra coluna definir dependendo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="791ac-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="791ac-125">Para obter uma lista completa das colunas em uma tabela de destinatário, consulte [Tabelas do destinatário](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="791ac-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="791ac-126">Algumas tabelas destinatários oferecem suporte a uma ampla variedade de restrições; outros não.</span><span class="sxs-lookup"><span data-stu-id="791ac-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="791ac-127">Suporte a restrições depende da implementação do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="791ac-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="791ac-128">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta as seguintes chamadas para a tabela de destinatários:</span><span class="sxs-lookup"><span data-stu-id="791ac-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="791ac-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="791ac-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="791ac-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="791ac-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="791ac-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="791ac-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="791ac-132">Definindo as solicitações de sinalizador Unicode que as informações de quaisquer colunas de cadeia de caracteres retornada dessas chamadas estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="791ac-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="791ac-133">No entanto, porque nem todos os provedores de armazenamento de mensagem oferecem suporte a Unicode, defina esse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="791ac-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="791ac-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="791ac-134">Notes to callers</span></span>

<span data-ttu-id="791ac-135">Você pode alterar uma tabela de destinatário, enquanto ela está aberta chamando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="791ac-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="791ac-136">**ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="791ac-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="791ac-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="791ac-137">See also</span></span>



[<span data-ttu-id="791ac-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="791ac-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="791ac-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="791ac-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="791ac-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="791ac-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="791ac-141">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="791ac-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

