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
ms.openlocfilehash: 4bc4d680903d81b51a39ed39db3861597443d116
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766692"
---
# <a name="handsoffaftersave-state"></a><span data-ttu-id="68712-103">Estado HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-103">HandsOffAfterSave State</span></span>

  
  
<span data-ttu-id="68712-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="68712-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="68712-105">O estado de HandsOffAfterSave faz parte do processo de salvar o conteúdo de um formulário em um armazenamento permanente.</span><span class="sxs-lookup"><span data-stu-id="68712-105">The HandsOffAfterSave state is part of the process of saving the contents of a form to permanent storage.</span></span> <span data-ttu-id="68712-106">Quando nesse estado, o objeto form deve Evite as alterações as cópias na memória dos valores das propriedades da mensagem, pois não pode ser outra oportunidade salvar estas alterações.</span><span class="sxs-lookup"><span data-stu-id="68712-106">When in this state, the form object should refrain from making changes to the in-memory copies of values of the message's properties, because there may not be another opportunity to save those changes.</span></span> <span data-ttu-id="68712-107">A tabela a seguir descreve as transições permitidas do estado de HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="68712-107">The following table describes allowed transitions from the HandsOffAfterSave state.</span></span>
  
|<span data-ttu-id="68712-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="68712-108">**IPersistMessage method**</span></span>|<span data-ttu-id="68712-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="68712-109">**Action**</span></span>|<span data-ttu-id="68712-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="68712-110">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68712-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) (_pMessage! =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="68712-111">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md)(_pMessage !=_ NULL)</span></span>  <br/> |<span data-ttu-id="68712-112">Abra quaisquer objetos incorporados.</span><span class="sxs-lookup"><span data-stu-id="68712-112">Open any embedded objects.</span></span> <span data-ttu-id="68712-113">Os dados na mensagem armazenado em _pMessage_ são garantidos para ser o mesmo que a mensagem na chamada [IPersistMessage::Save](ipersistmessage-save.md) anterior.</span><span class="sxs-lookup"><span data-stu-id="68712-113">The data in the message stored in  _pMessage_ is guaranteed to be the same as the message in the previous [IPersistMessage::Save](ipersistmessage-save.md) call.</span></span> <span data-ttu-id="68712-114">Se a chamada **SaveCompleted** tiver êxito, insira o estado Normal.</span><span class="sxs-lookup"><span data-stu-id="68712-114">If the **SaveCompleted** call succeeds, enter the Normal state.</span></span> <span data-ttu-id="68712-115">Caso contrário, defina o último erro para E_OUTOFMEMORY e permanecer no estado HandsOffAfterSave.</span><span class="sxs-lookup"><span data-stu-id="68712-115">Otherwise, set the last error to E_OUTOFMEMORY and stay in the HandsOffAfterSave state.</span></span>  <br/> |<span data-ttu-id="68712-116">[Normal](normal-state.md) ou HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-116">[Normal](normal-state.md) or HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="68712-117">**IPersistMessage::SaveCompleted** (_pMessage = =_ nulo)</span><span class="sxs-lookup"><span data-stu-id="68712-117">**IPersistMessage::SaveCompleted**(_pMessage ==_ NULL)</span></span>  <br/> |<span data-ttu-id="68712-118">Defina o último erro E_INVALIDARG ou E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="68712-118">Set the last error to E_INVALIDARG or E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="68712-119">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-119">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="68712-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Salvar**ou [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span><span class="sxs-lookup"><span data-stu-id="68712-120">[IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md), **Save**, or [IPersistMessage::InitNew](ipersistmessage-initnew.md)</span></span> <br/> |<span data-ttu-id="68712-121">Defina o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="68712-121">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="68712-122">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-122">HandsOffAfterSave</span></span>  <br/> |
|[<span data-ttu-id="68712-123">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="68712-123">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="68712-124">Carregar o objeto de formulário com os dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="68712-124">Load the form object with data from the target message.</span></span> <span data-ttu-id="68712-125">Essa chamada pode ocorrer quando o objeto de formulário será a mensagem anterior ou seguinte em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="68712-125">This call can occur when the form object is going to the next or previous message in a folder.</span></span>  <br/> |<span data-ttu-id="68712-126">Normal</span><span class="sxs-lookup"><span data-stu-id="68712-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="68712-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="68712-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="68712-128">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="68712-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="68712-129">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-129">HandsOffAfterSave</span></span>  <br/> |
|<span data-ttu-id="68712-130">Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="68712-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="68712-131">Defina o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="68712-131">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="68712-132">HandsOffAfterSave</span><span class="sxs-lookup"><span data-stu-id="68712-132">HandsOffAfterSave</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68712-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="68712-133">See also</span></span>



[<span data-ttu-id="68712-134">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="68712-134">Form States</span></span>](form-states.md)

