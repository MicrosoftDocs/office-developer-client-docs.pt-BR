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
ms.openlocfilehash: 90ae9cee915296475d7fe64952b40ab7344e89e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767382"
---
# <a name="imessagegetrecipienttable"></a><span data-ttu-id="7be61-103">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="7be61-103">IMessage::GetRecipientTable</span></span>

  
  
<span data-ttu-id="7be61-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7be61-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7be61-105">Retorna a tabela de destinatário da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7be61-105">Returns the message's recipient table.</span></span>
  
```cpp
HRESULT GetRecipientTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="7be61-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="7be61-106">Parameters</span></span>

 <span data-ttu-id="7be61-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7be61-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7be61-108">[in] Bitmask dos sinalizadores que controla o retorno da tabela.</span><span class="sxs-lookup"><span data-stu-id="7be61-108">[in] Bitmask of flags that controls the return of the table.</span></span> <span data-ttu-id="7be61-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="7be61-109">The following flags can be set:</span></span>
    
<span data-ttu-id="7be61-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7be61-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7be61-111">Permite que **GetRecipientTable** retornar com êxito, possivelmente antes que a tabela é totalmente disponível para o cliente da chamada.</span><span class="sxs-lookup"><span data-stu-id="7be61-111">Allows **GetRecipientTable** to return successfully, possibly before the table is fully available to the calling client.</span></span> <span data-ttu-id="7be61-112">Se a tabela não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro.</span><span class="sxs-lookup"><span data-stu-id="7be61-112">If the table is not available, making a subsequent call to it can cause an error.</span></span> 
    
<span data-ttu-id="7be61-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7be61-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7be61-114">Colunas de cadeia de caracteres devem estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7be61-114">String columns should be in Unicode format.</span></span> <span data-ttu-id="7be61-115">Se o sinalizador MAPI_UNICODE não estiver definido, as colunas de cadeia de caracteres devem estar no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="7be61-115">If the MAPI_UNICODE flag is not set, the string columns should be in ANSI format.</span></span>
    
 <span data-ttu-id="7be61-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="7be61-116">_lppTable_</span></span>
  
> <span data-ttu-id="7be61-117">[out] Ponteiro para um ponteiro para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="7be61-117">[out] Pointer to a pointer to the recipient table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7be61-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7be61-118">Return value</span></span>

<span data-ttu-id="7be61-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7be61-119">S_OK</span></span> 
  
> <span data-ttu-id="7be61-120">A tabela de destinatários foi retornada com êxito.</span><span class="sxs-lookup"><span data-stu-id="7be61-120">The recipient table was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7be61-121">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="7be61-121">Remarks</span></span>

<span data-ttu-id="7be61-122">O método **IMessage::GetRecipientTable** retorna um ponteiro para a tabela de destinatário da mensagem, que inclui informações sobre todos os destinatários da mensagem.</span><span class="sxs-lookup"><span data-stu-id="7be61-122">The **IMessage::GetRecipientTable** method returns a pointer to the message's recipient table, which includes information about all of the recipients for the message.</span></span> <span data-ttu-id="7be61-123">Não há uma linha para cada destinatário.</span><span class="sxs-lookup"><span data-stu-id="7be61-123">There is one row for every recipient.</span></span> 
  
<span data-ttu-id="7be61-124">Tabelas de destinatários têm outra coluna definir dependendo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="7be61-124">Recipient tables have a different column set depending on whether the message has been submitted.</span></span> <span data-ttu-id="7be61-125">Para obter uma lista completa das colunas em uma tabela de destinatário, consulte [Tabelas do destinatário](recipient-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7be61-125">For a complete list of the columns in a recipient table, see [Recipient Tables](recipient-tables.md).</span></span>
  
<span data-ttu-id="7be61-126">Algumas tabelas destinatários oferecem suporte a uma ampla variedade de restrições; outros não.</span><span class="sxs-lookup"><span data-stu-id="7be61-126">Some recipient tables support a wide variety of restrictions; others do not.</span></span> <span data-ttu-id="7be61-127">Suporte a restrições depende da implementação do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="7be61-127">Support for restrictions depends on the message store provider's implementation.</span></span> 
  
<span data-ttu-id="7be61-128">Definir o sinalizador MAPI_UNICODE no parâmetro _ulFlags_ afeta as seguintes chamadas para a tabela de destinatários:</span><span class="sxs-lookup"><span data-stu-id="7be61-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the following calls to the recipient table:</span></span> 
  
- <span data-ttu-id="7be61-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) para recuperar o conjunto de coluna.</span><span class="sxs-lookup"><span data-stu-id="7be61-129">[IMAPITable::QueryColumns](imapitable-querycolumns.md) to retrieve the column set.</span></span> 
    
- <span data-ttu-id="7be61-130">[IMAPITable:: QueryRows](imapitable-queryrows.md) para recuperar linhas.</span><span class="sxs-lookup"><span data-stu-id="7be61-130">[IMAPITable::QueryRows](imapitable-queryrows.md) to retrieve rows.</span></span> 
    
- <span data-ttu-id="7be61-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) para recuperar a ordem de classificação.</span><span class="sxs-lookup"><span data-stu-id="7be61-131">[IMAPITable::QuerySortOrder](imapitable-querysortorder.md) to retrieve the sort order.</span></span> 
    
<span data-ttu-id="7be61-132">Definindo as solicitações de sinalizador Unicode que as informações de quaisquer colunas de cadeia de caracteres retornada dessas chamadas estar no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="7be61-132">Setting the Unicode flag requests that the information for any string columns returned from these calls be in Unicode format.</span></span> <span data-ttu-id="7be61-133">No entanto, porque nem todos os provedores de armazenamento de mensagem oferecem suporte a Unicode, defina esse sinalizador é apenas uma solicitação.</span><span class="sxs-lookup"><span data-stu-id="7be61-133">However, because not all message store providers support Unicode, setting this flag is only a request.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7be61-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="7be61-134">Notes to callers</span></span>

<span data-ttu-id="7be61-135">Você pode alterar uma tabela de destinatário, enquanto ela está aberta chamando o método [IMessage::ModifyRecipients](imessage-modifyrecipients.md) .</span><span class="sxs-lookup"><span data-stu-id="7be61-135">You can change a recipient table while it is open by calling the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method.</span></span> <span data-ttu-id="7be61-136">**ModifyRecipients** adiciona destinatários, exclui destinatários ou modifica as propriedades do destinatário.</span><span class="sxs-lookup"><span data-stu-id="7be61-136">**ModifyRecipients** adds recipients, deletes recipients, or modifies recipient properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7be61-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="7be61-137">See also</span></span>



[<span data-ttu-id="7be61-138">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="7be61-138">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="7be61-139">IMAPITable:: QueryRows</span><span class="sxs-lookup"><span data-stu-id="7be61-139">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7be61-140">IMessage::ModifyRecipients</span><span class="sxs-lookup"><span data-stu-id="7be61-140">IMessage::ModifyRecipients</span></span>](imessage-modifyrecipients.md)
  
[<span data-ttu-id="7be61-141">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7be61-141">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

