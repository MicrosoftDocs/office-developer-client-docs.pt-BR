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
ms.openlocfilehash: 92c604c621e2837b76e9e49fd182524ad17fbcac
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588339"
---
# <a name="handsofffromnormal-state"></a><span data-ttu-id="938af-103">Estado HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-103">HandsOffFromNormal State</span></span>

  
  
<span data-ttu-id="938af-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="938af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="938af-105">O estado de HandsOffFromNormal é muito similar ao estado [HandsOffAfterSave](handsoffaftersave-state.md) .</span><span class="sxs-lookup"><span data-stu-id="938af-105">The HandsOffFromNormal state is very similar to the [HandsOffAfterSave](handsoffaftersave-state.md) state.</span></span> <span data-ttu-id="938af-106">Ele faz parte do processo de salvar o conteúdo de um formulário em um armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="938af-106">It is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="938af-107">Quando nesse estado, o objeto form deve Evite as alterações as cópias na memória dos valores das propriedades da mensagem, pois não pode ser outra oportunidade salvar estas alterações.</span><span class="sxs-lookup"><span data-stu-id="938af-107">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="938af-108">A tabela a seguir descreve as transições permitidas do estado de HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="938af-108">The following table describes allowed transitions from the HandsOffFromNormal state.</span></span> 
  
|<span data-ttu-id="938af-109">IPersistMessage * * método * *</span><span class="sxs-lookup"><span data-stu-id="938af-109">****IPersistMessage** method**</span></span>|<span data-ttu-id="938af-110">**Action**</span><span class="sxs-lookup"><span data-stu-id="938af-110">**Action**</span></span>|<span data-ttu-id="938af-111">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="938af-111">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="938af-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="938af-112">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="938af-113">Substitua mensagem do objeto mensagem _pMessage_, que é a substituição da mensagem revogado pela chamada anterior à [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span><span class="sxs-lookup"><span data-stu-id="938af-113">Replace the message object's message with  _pMessage_, which is the replacement for the message revoked by the previous call to [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md).</span></span> <span data-ttu-id="938af-114">São garantidos que os dados na nova mensagem ser os mesmos que a mensagem revogada.</span><span class="sxs-lookup"><span data-stu-id="938af-114">The data in the new message is guaranteed to be the same as in the revoked message.</span></span> <span data-ttu-id="938af-115">A mensagem não deve ser marcada como limpar, nem [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) deve ser chamado após essa chamada.</span><span class="sxs-lookup"><span data-stu-id="938af-115">The message should not be marked as clean, nor should [IMAPIViewAdviseSink::OnSaved](imapiviewadvisesink-onsaved.md) be called after this call.</span></span> <span data-ttu-id="938af-116">Se a chamada **SaveCompleted** tiver êxito, insira o estado [Normal](normal-state.md) .</span><span class="sxs-lookup"><span data-stu-id="938af-116">If the **SaveCompleted** call succeeds, enter the [Normal](normal-state.md) state.</span></span> <span data-ttu-id="938af-117">Caso contrário, mantenha-se no estado HandsOffFromNormal.</span><span class="sxs-lookup"><span data-stu-id="938af-117">Otherwise, stay in the HandsOffFromNormal state.</span></span>  <br/> |<span data-ttu-id="938af-118">Normal ou HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-118">Normal or HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="938af-119">**IPersistMessage::SaveCompleted** (_pMessage = =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="938af-119">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="938af-120">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="938af-120">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="938af-121">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-121">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="938af-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md)ou [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="938af-122">**HandsOffMessage**, [IPersistMessage::Save](ipersistmessage-save.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md), or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="938af-123">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="938af-123">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="938af-124">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-124">HandsOffFromNormal</span></span>  <br/> |
|[<span data-ttu-id="938af-125">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="938af-125">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="938af-126">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="938af-126">Return the last error.</span></span>  <br/> |<span data-ttu-id="938af-127">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-127">HandsOffFromNormal</span></span>  <br/> |
|<span data-ttu-id="938af-128">Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="938af-128">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="938af-129">Defina o último erro como E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="938af-129">Set the last error to E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="938af-130">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="938af-130">HandsOffFromNormal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="938af-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="938af-131">See also</span></span>



[<span data-ttu-id="938af-132">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="938af-132">Form States</span></span>](form-states.md)

