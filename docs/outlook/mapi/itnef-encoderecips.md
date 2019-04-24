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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348654"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="e35a5-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="e35a5-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="e35a5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e35a5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e35a5-105">Codifica um modo de exibição da tabela de destinatários de uma mensagem no fluxo de dados do formato de encapsulamento de transporte neutro (TNEF) para a mensagem.</span><span class="sxs-lookup"><span data-stu-id="e35a5-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="e35a5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e35a5-106">Parameters</span></span>

 <span data-ttu-id="e35a5-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e35a5-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e35a5-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e35a5-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e35a5-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="e35a5-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="e35a5-110">no Um ponteiro para a tabela de destinatários para a qual o modo de exibição é codificado.</span><span class="sxs-lookup"><span data-stu-id="e35a5-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="e35a5-111">O parâmetro _lpRecipientTable_ pode ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e35a5-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e35a5-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e35a5-112">Return value</span></span>

<span data-ttu-id="e35a5-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="e35a5-113">S_OK</span></span> 
  
> <span data-ttu-id="e35a5-114">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e35a5-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e35a5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e35a5-115">Remarks</span></span>

<span data-ttu-id="e35a5-116">Provedores de transporte, provedores de repositórios de mensagens e gateways chamam o método **ITnef:: EncodeRecips** para executar a codificação TNEF para um determinado modo de exibição de tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="e35a5-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="e35a5-117">A codificação TNEF é útil, por exemplo, se um provedor ou gateway exigir um determinado conjunto de colunas, ordem de classificação ou restrição para a tabela de destinatários.</span><span class="sxs-lookup"><span data-stu-id="e35a5-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="e35a5-118">Um provedor ou gateway passa o modo de exibição de tabela a ser codificado no parâmetro _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="e35a5-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="e35a5-119">A implementação do TNEF codifica a tabela de destinatários com o modo de exibição fornecido, usando o conjunto de colunas determinado, a ordem de classificação, a restrição e a posição.</span><span class="sxs-lookup"><span data-stu-id="e35a5-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="e35a5-120">Se um provedor ou gateway passar nulos no _lpRecipientTable_, o TNEF Obtém a tabela de destinatários da mensagem que está sendo codificada usando o método [IMessage::](imessage-getrecipienttable.md) GetRecipientTable e processa todas as linhas da tabela para o fluxo TNEF usando o configurações atuais da tabela.</span><span class="sxs-lookup"><span data-stu-id="e35a5-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="e35a5-121">Chamar **EncodeRecips** com nulo no _lpRecipientTable_ , portanto, codifica todos os destinatários da mensagem e é equivalente a chamar o método [ITnef::](itnef-addprops.md) addprops com o sinalizador TNEF_PROP_INCLUDE em seu parâmetro _parâmetroulflags_ e o **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) propriedade em seu parâmetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="e35a5-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="e35a5-122">Observe que raramente é necessário chamar o **EncodeRecips** , a menos que haja um requisito para codificar um modo de exibição de tabela de destinatário específico.</span><span class="sxs-lookup"><span data-stu-id="e35a5-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="e35a5-123">Os sistemas de mensagens estrangeiras quase sempre têm recursos para lidar com listas de destinatários que são poderosas o suficiente para lidar com as necessidades comuns de codificar listas de destinatários; Portanto, esses sistemas quase nunca exigem o TNEF para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="e35a5-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e35a5-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="e35a5-124">See also</span></span>



[<span data-ttu-id="e35a5-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="e35a5-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="e35a5-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="e35a5-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="e35a5-127">Propriedade canônica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="e35a5-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="e35a5-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e35a5-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

