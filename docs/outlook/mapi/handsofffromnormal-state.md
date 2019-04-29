---
title: Estado HandsOffFromNormal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1afe6a2e-a5e6-4844-9f82-908894fc6759
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 17fa0f3d4e74ce7d717a94378880f2cc46150fc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426468"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="fd9e8-103">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="fd9e8-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd9e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd9e8-105">O estado HandsOffFromNormal é muito semelhante ao estado [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="fd9e8-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="fd9e8-106">Ele faz parte do processo de salvar o conteúdo de um formulário no armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="fd9e8-107">Quando nesse estado, o objeto Form deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="fd9e8-108">A tabela a seguir descreve as transições permitidas do estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="fd9e8-109">IPersistMessage \* \* método \* \*</span><span class="sxs-lookup"><span data-stu-id="fd9e8-109">\*\*\*\*IPersistMessage\*\* method\*\*</span></span>|<span data-ttu-id="fd9e8-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="fd9e8-110">**Action**</span></span>|<span data-ttu-id="fd9e8-111">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="fd9e8-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd9e8-112">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_PMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="fd9e8-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="fd9e8-113">Substitua a mensagem do objeto Message por _PMessage_, que é a substituição da mensagem revogada pela chamada anterior a [IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="fd9e8-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="fd9e8-114">É garantido que os dados na nova mensagem sejam iguais aos da mensagem revogada.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="fd9e8-115">A mensagem não deve ser marcada como limpa, nem [IMAPIViewAdviseSink::](imapiviewadvisesink-onsaved.md) onsaved deve ser chamado após esta chamada.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="fd9e8-116">Se a chamada **SaveCompleted** for bem-sucedida, insira o estado [normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="fd9e8-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="fd9e8-117">Caso contrário, permaneça no estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="fd9e8-118">Normal ou HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="fd9e8-119">**IPersistMessage:: SaveCompleted** (_PMessage = =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="fd9e8-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="fd9e8-120">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fd9e8-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="fd9e8-122">**HandsOffMessage**, [IPersistMessage:: salvar](ipersistmessage-save.md), [IPersistMessage:: InitNew](ipersistmessage-initnew.md)ou [IPersistMessage:: Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="fd9e8-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="fd9e8-123">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fd9e8-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="fd9e8-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="fd9e8-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="fd9e8-126">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="fd9e8-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="fd9e8-128">Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="fd9e8-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="fd9e8-129">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="fd9e8-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="fd9e8-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="fd9e8-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd9e8-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd9e8-131">See also</span></span>



[<span data-ttu-id="fd9e8-132">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="fd9e8-132">Form States</span></span>](form-states.md)

