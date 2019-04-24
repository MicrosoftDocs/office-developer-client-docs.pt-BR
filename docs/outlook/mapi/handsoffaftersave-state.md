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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299521"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="8cf14-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="8cf14-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8cf14-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8cf14-105">O estado HandsOffAfterSave é parte do processo de salvar o conteúdo de um formulário no armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="8cf14-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="8cf14-106">Quando nesse estado, o objeto Form deve evitar fazer alterações nas cópias na memória dos valores das propriedades da mensagem, porque pode não haver outra oportunidade para salvar essas alterações.</span><span class="sxs-lookup"><span data-stu-id="8cf14-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="8cf14-107">A tabela a seguir descreve as transições permitidas do estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="8cf14-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="8cf14-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="8cf14-108">**IPersistMessage method**</span></span>|<span data-ttu-id="8cf14-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="8cf14-109">**Action**</span></span>|<span data-ttu-id="8cf14-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="8cf14-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cf14-111">[IPersistMessage:: SaveCompleted](ipersistmessage-savecompleted.md) (_PMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="8cf14-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="8cf14-112">Abra quaisquer objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="8cf14-112">Open any embedded objects.</span></span> <span data-ttu-id="8cf14-113">É garantido que os dados da mensagem armazenada no _PMessage_ sejam iguais à mensagem do [IPersistMessage anterior:: salvar](ipersistmessage-save.md) chamada.</span><span class="sxs-lookup"><span data-stu-id="8cf14-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="8cf14-114">Se a chamada **SaveCompleted** for bem-sucedida, insira o estado normal.</span><span class="sxs-lookup"><span data-stu-id="8cf14-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="8cf14-115">Caso contrário, defina o último erro como E_OUTOFMEMORY e permaneça no estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="8cf14-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="8cf14-116">[Normal](normal-state.md) ou HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8cf14-117">**IPersistMessage:: SaveCompleted** (_PMessage = =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="8cf14-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="8cf14-118">Defina o último erro como E_INVALIDARG ou E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8cf14-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8cf14-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8cf14-120">[IPersistMessage:: HandsOffMessage](ipersistmessage-handsoffmessage.md), **salvar**ou [IPersistMessage:: InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="8cf14-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="8cf14-121">Definir o último erro para e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8cf14-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8cf14-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="8cf14-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="8cf14-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="8cf14-124">Carregar o objeto Form com dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="8cf14-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="8cf14-125">Essa chamada pode ocorrer quando o objeto Form estiver indo para a mensagem seguinte ou anterior em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="8cf14-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="8cf14-126">Normal</span><span class="sxs-lookup"><span data-stu-id="8cf14-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="8cf14-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="8cf14-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="8cf14-128">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="8cf14-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="8cf14-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="8cf14-130">Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="8cf14-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="8cf14-131">Definir o último erro para e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="8cf14-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="8cf14-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="8cf14-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8cf14-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="8cf14-133">See also</span></span>



[<span data-ttu-id="8cf14-134">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="8cf14-134">Form States</span></span>](form-states.md)

