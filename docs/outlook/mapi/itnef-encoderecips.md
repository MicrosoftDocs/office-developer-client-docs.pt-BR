---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767720"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="9d80f-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="9d80f-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="9d80f-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9d80f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9d80f-105">Codifica um modo de exibição da tabela do destinatário da mensagem o fluxo de dados Transport-Neutral Encapsulation Format (TNEF) para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="9d80f-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="9d80f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9d80f-106">Parameters</span></span>

 <span data-ttu-id="9d80f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9d80f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9d80f-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="9d80f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9d80f-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="9d80f-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="9d80f-110">[in] Um ponteiro para a tabela de destinatários para os quais o modo de exibição é codificado.</span><span class="sxs-lookup"><span data-stu-id="9d80f-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="9d80f-111">O parâmetro _lpRecipientTable_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="9d80f-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9d80f-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9d80f-112">Return value</span></span>

<span data-ttu-id="9d80f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d80f-113">S_OK</span></span> 
  
> <span data-ttu-id="9d80f-114">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="9d80f-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9d80f-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d80f-115">Remarks</span></span>

<span data-ttu-id="9d80f-116">Transporte provedores, provedores de armazenamento de mensagem e o método **ITnef::EncodeRecips** de chamada de gateways para executar a codificação TNEF para um modo de exibição de tabela de destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="9d80f-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="9d80f-117">A codificação TNEF é útil, por exemplo, se um provedor ou gateway exige um conjunto específico de colunas, ordem de classificação ou restrição para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="9d80f-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="9d80f-118">Um provedor ou gateway passa o modo de exibição de tabela a ser codificada no parâmetro _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="9d80f-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="9d80f-119">A implementação de TNEF codifica a tabela de destinatários com o modo de exibição específico, usando o conjunto específico de colunas, ordem de classificação, restrição e posição.</span><span class="sxs-lookup"><span data-stu-id="9d80f-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="9d80f-120">Se um provedor ou gateway transmite NULL no _lpRecipientTable_, TNEF obtém uma tabela de destinatário da mensagem que está sendo codificada usando o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) , processos e todas as linhas da tabela no fluxo TNEF usando o configurações atuais da tabela.</span><span class="sxs-lookup"><span data-stu-id="9d80f-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="9d80f-121">Assim, chamando **EncodeRecips** com NULL em _lpRecipientTable_ codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE no seu parâmetro _ulFlags_ e o **PR_ MESSAGE_RECIPIENTS** propriedade ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) no seu parâmetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="9d80f-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="9d80f-122">Observe que é raramente necessário chamar **EncodeRecips** , a menos que haja um requisito para codificar um modo de exibição de tabela de destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="9d80f-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="9d80f-123">Sistemas de mensagens estrangeiro quase sempre têm instalações de manipulação de destinatários listas que são potentes o suficiente para atender às necessidades comuns de codificação de listas de destinatário; Portanto, esses sistemas quase nunca requerem o TNEF para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="9d80f-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9d80f-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d80f-124">See also</span></span>



[<span data-ttu-id="9d80f-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="9d80f-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="9d80f-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="9d80f-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="9d80f-127">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="9d80f-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="9d80f-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9d80f-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

