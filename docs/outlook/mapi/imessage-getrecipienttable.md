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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ca42e91528cdb7e61ae3620989c4a89966db1061
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424606"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="0ba79-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="0ba79-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="0ba79-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ba79-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ba79-105">Retorna a tabela de destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ba79-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="0ba79-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0ba79-106">Parameters</span></span>

 <span data-ttu-id="0ba79-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0ba79-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0ba79-108">no Bitmask dos sinalizadores que controlam o retorno da tabela.</span><span class="sxs-lookup"><span data-stu-id="0ba79-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="0ba79-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="0ba79-109">The following flags can be set:</span></span>
    
<span data-ttu-id="0ba79-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="0ba79-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="0ba79-111">Permite \*\*\*\* que GetRecipientTable seja retornado com êxito, possivelmente antes que a tabela esteja totalmente disponível para o cliente de chamada.</span><span class="sxs-lookup"><span data-stu-id="0ba79-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="0ba79-112">Se a tabela não estiver disponível, fazer uma chamada subsequente para ela pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="0ba79-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="0ba79-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0ba79-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0ba79-114">As colunas de cadeia de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ba79-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="0ba79-115">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="0ba79-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="0ba79-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="0ba79-116">_lppTable_</span></span>
  
> <span data-ttu-id="0ba79-117">bota Ponteiro para um ponteiro para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="0ba79-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0ba79-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0ba79-118">Return value</span></span>

<span data-ttu-id="0ba79-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ba79-119">S_OK</span></span> 
  
> <span data-ttu-id="0ba79-120">A tabela de destinatários foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="0ba79-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0ba79-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="0ba79-121">Remarks</span></span>

<span data-ttu-id="0ba79-122">O método **IMessage::** GetRecipientTable Retorna um ponteiro para a tabela de destinatários da mensagem, que inclui informações sobre todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="0ba79-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="0ba79-123">Há uma linha para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="0ba79-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="0ba79-124">As tabelas de destinatários têm um conjunto de colunas diferente, dependendo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="0ba79-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="0ba79-125">Para obter uma lista completa das colunas em uma tabela de destinatários, consulte [tabelas de destinatários](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="0ba79-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="0ba79-126">Algumas tabelas de destinatários dão suporte a uma ampla variedade de restrições; outros não.</span><span class="sxs-lookup"><span data-stu-id="0ba79-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="0ba79-127">O suporte para restrições depende da implementação do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="0ba79-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="0ba79-128">Definir o sinalizador MAPI_UNICODE no parâmetro _parâmetroulflags_ afeta as seguintes chamadas para a tabela de destinatários:</span><span class="sxs-lookup"><span data-stu-id="0ba79-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="0ba79-129">[IMAPITable:: QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de colunas.</span><span class="sxs-lookup"><span data-stu-id="0ba79-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="0ba79-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="0ba79-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="0ba79-131">[IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="0ba79-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="0ba79-132">Definir o sinalizador Unicode solicita que as informações de qualquer coluna de cadeia de caracteres retornada dessas chamadas estejam no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="0ba79-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="0ba79-133">No enTanto, como nem todos os provedores de repositórios de mensagens dão suporte a Unicode, a configuração desse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="0ba79-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="0ba79-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="0ba79-134">Notes to callers</span></span>

<span data-ttu-id="0ba79-135">Você pode alterar uma tabela de destinatários enquanto ela estiver aberta chamando o método [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="0ba79-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="0ba79-136">O **ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="0ba79-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0ba79-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="0ba79-137">See also</span></span>



[<span data-ttu-id="0ba79-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="0ba79-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="0ba79-139">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="0ba79-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="0ba79-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="0ba79-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="0ba79-141">IMessage : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="0ba79-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

