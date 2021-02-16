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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437648"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="81967-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="81967-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="81967-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="81967-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="81967-105">Codifica uma exibição para a tabela de destinatários de uma mensagem no fluxo de dados TNEF (Formato de Encapsulamento Transport-Neutral) da mensagem.</span><span class="sxs-lookup"><span data-stu-id="81967-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="81967-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="81967-106">Parameters</span></span>

 <span data-ttu-id="81967-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="81967-107">_ulFlags_</span></span>
  
> <span data-ttu-id="81967-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="81967-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="81967-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="81967-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="81967-110">[in] Um ponteiro para a tabela de destinatários para a qual o exibição é codificado.</span><span class="sxs-lookup"><span data-stu-id="81967-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="81967-111">O  _parâmetro lpRecipientTable_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="81967-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="81967-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="81967-112">Return value</span></span>

<span data-ttu-id="81967-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="81967-113">S_OK</span></span> 
  
> <span data-ttu-id="81967-114">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="81967-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="81967-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="81967-115">Remarks</span></span>

<span data-ttu-id="81967-116">Provedores de transporte, provedores de armazenamento de mensagens e gateways chamam o método **ITnef::EncodeRecips** para executar a codificação TNEF para um modo de exibição de tabela de destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="81967-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="81967-117">A codificação TNEF é útil, por exemplo, se um provedor ou gateway exigir um determinado conjunto de colunas, ordem de classificação ou restrição para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="81967-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="81967-118">Um provedor ou gateway passa o ponto de vista da tabela para ser codificado no parâmetro _lpRecipientTable._</span><span class="sxs-lookup"><span data-stu-id="81967-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="81967-119">A implementação do TNEF codifica a tabela de destinatários com o modo de exibição determinado, usando o conjunto de colunas determinado, a ordem de classificação, a restrição e a posição.</span><span class="sxs-lookup"><span data-stu-id="81967-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="81967-120">Se um provedor ou gateway passar NULL em  _lpRecipientTable_, TNEF obtém a tabela de destinatário da mensagem que está sendo codificada usando o método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) e processa todas as linhas da tabela para o fluxo TNEF usando as configurações atuais da tabela.</span><span class="sxs-lookup"><span data-stu-id="81967-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="81967-121">Chamar **EncodeRecips** com NULL em _lpRecipientTable_ codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::AddProps](itnef-addprops.md) com o sinalizador TNEF_PROP_INCLUDE em _seu parâmetro ulFlags_ e a propriedade **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) em seu parâmetro _lpPropList._</span><span class="sxs-lookup"><span data-stu-id="81967-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="81967-122">Observe que raramente é necessário chamar **EncodeRecips,** a menos que haja um requisito para codificar um determinado exibição de tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="81967-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="81967-123">Sistemas de mensagens estrangeiros quase sempre têm instalações para lidar com listas de destinatários que são poderosas o suficiente para lidar com as necessidades comuns de codificação de listas de destinatários; portanto, esses sistemas quase nunca exigem TNEF para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="81967-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="81967-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="81967-124">See also</span></span>



[<span data-ttu-id="81967-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="81967-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="81967-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="81967-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="81967-127">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="81967-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="81967-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="81967-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

