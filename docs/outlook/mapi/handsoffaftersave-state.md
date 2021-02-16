---
title: Estado HandsOffAfterSave
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ffdfed49-2c52-445c-8051-6e566f61eedc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 85630965c7e78e6fa76e348bfe98cc9060665057
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406602"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="14f85-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="14f85-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="14f85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="14f85-105">O estado HandsOffAfterSave faz parte do processo de salvar o conteúdo de um formulário em armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="14f85-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="14f85-106">Nesse estado, o objeto de formulário deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="14f85-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="14f85-107">A tabela a seguir descreve transições permitidas do estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="14f85-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="14f85-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="14f85-108">**IPersistMessage method**</span></span>|<span data-ttu-id="14f85-109">**Ação**</span><span class="sxs-lookup"><span data-stu-id="14f85-109">**Action**</span></span>|<span data-ttu-id="14f85-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="14f85-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="14f85-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span><span class="sxs-lookup"><span data-stu-id="14f85-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="14f85-112">Abra todos os objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="14f85-112">Open any embedded objects.</span></span> <span data-ttu-id="14f85-113">Os dados na mensagem armazenada em  _pMessage_ são garantidos como os mesmos da mensagem na chamada [IPersistMessage::Save](ipersistmessage-save.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="14f85-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="14f85-114">Se a **chamada SaveCompleted** for bem-sucedida, insira o estado Normal.</span><span class="sxs-lookup"><span data-stu-id="14f85-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="14f85-115">Caso contrário, de definida a última E_OUTOFMEMORY e fique no estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="14f85-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="14f85-116">[Normal](normal-state.md) ou HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="14f85-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span><span class="sxs-lookup"><span data-stu-id="14f85-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="14f85-118">De definir o último erro como E_INVALIDARG ou E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="14f85-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="14f85-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="14f85-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save** ou [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="14f85-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="14f85-121">De definida a última mensagem de erro e retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="14f85-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="14f85-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="14f85-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="14f85-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="14f85-124">Carregue o objeto de formulário com dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="14f85-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="14f85-125">Essa chamada pode ocorrer quando o objeto de formulário está indo para a mensagem seguinte ou anterior em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="14f85-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="14f85-126">Normal</span><span class="sxs-lookup"><span data-stu-id="14f85-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="14f85-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="14f85-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="14f85-128">Retornar o último erro.</span><span class="sxs-lookup"><span data-stu-id="14f85-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="14f85-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="14f85-130">Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="14f85-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="14f85-131">De definida a última mensagem de erro e retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="14f85-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="14f85-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="14f85-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="14f85-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="14f85-133">See also</span></span>



[<span data-ttu-id="14f85-134">Estados do formulário</span><span class="sxs-lookup"><span data-stu-id="14f85-134">Form States</span></span>](form-states.md)

