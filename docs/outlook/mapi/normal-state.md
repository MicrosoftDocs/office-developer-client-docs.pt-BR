---
title: Estado Normal
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b2acad7-5ef8-44db-911f-3bd2a7ca2778
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dcc92d220f07b1c111284acacac4a65a2e3f8b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768151"
---
# <a name="normal-state"></a><span data-ttu-id="91924-103">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="91924-103">Normal State</span></span>

  
  
<span data-ttu-id="91924-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="91924-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="91924-105">O estado Normal é onde o objeto form passa a maior parte de seu tempo, aguardando para aplicativos de cliente para iniciar uma ação como salvar as alterações ou fechar o formulário.</span><span class="sxs-lookup"><span data-stu-id="91924-105">The Normal state is where the form object spends most of its time, waiting for client applications to initiate an action such as saving changes or closing the form.</span></span> <span data-ttu-id="91924-106">A tabela a seguir descreve as transições permitidas do estado Normal.</span><span class="sxs-lookup"><span data-stu-id="91924-106">The following table describes allowed transitions from the Normal state.</span></span>
  
|<span data-ttu-id="91924-107">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="91924-107">**IPersistMessage method**</span></span>|<span data-ttu-id="91924-108">**Action**</span><span class="sxs-lookup"><span data-stu-id="91924-108">**Action**</span></span>|<span data-ttu-id="91924-109">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="91924-109">**New state**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91924-110">[IPersistMessage::Save](ipersistmessage-save.md) (_pMessage = =_ nula _fSameAsLoad = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="91924-110">[IPersistMessage::Save](ipersistmessage-save.md)(_pMessage ==_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> <span data-ttu-id="91924-111">-ou-</span><span class="sxs-lookup"><span data-stu-id="91924-111">-or-</span></span>  <br/> <span data-ttu-id="91924-112">**IPersistMessage::Save** (_pMessage! =_ nula _fSameAsLoad = =_ falso)</span><span class="sxs-lookup"><span data-stu-id="91924-112">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ FALSE)</span></span>  <br/> |<span data-ttu-id="91924-113">Recursivamente salvar quaisquer objetos OLE incorporados que foram modificados.</span><span class="sxs-lookup"><span data-stu-id="91924-113">Recursively save any embedded OLE objects that have been modified.</span></span> <span data-ttu-id="91924-114">Salve dados de mensagem volta para o objeto de mensagem.</span><span class="sxs-lookup"><span data-stu-id="91924-114">Save message data back to the message object.</span></span> <span data-ttu-id="91924-115">Armazene o sinalizador _fSameAsLoad_ para uso posterior no estado [NoScribble](noscribble-state.md) .</span><span class="sxs-lookup"><span data-stu-id="91924-115">Store the  _fSameAsLoad_ flag for later use in the [NoScribble](noscribble-state.md) state.</span></span>  <br/> |<span data-ttu-id="91924-116">NoScribble</span><span class="sxs-lookup"><span data-stu-id="91924-116">NoScribble</span></span>  <br/> |
|<span data-ttu-id="91924-117">**IPersistMessage::Save** (_pMessage! =_ nula _fSameAsLoad = =_ TRUE)</span><span class="sxs-lookup"><span data-stu-id="91924-117">**IPersistMessage::Save**(_pMessage !=_ NULL,  _fSameAsLoad ==_ TRUE)</span></span>  <br/> |<span data-ttu-id="91924-118">Isso é o mesmo caso anterior, exceto pelo fato dessa chamada **Salvar** é usada em situações de pouca memória e não deve transferir por falta de memória.</span><span class="sxs-lookup"><span data-stu-id="91924-118">This is the same as the previous case, except that this **Save** call is used in low-memory situations and must not fail for lack of memory.</span></span>  <br/> |<span data-ttu-id="91924-119">NoScribble</span><span class="sxs-lookup"><span data-stu-id="91924-119">NoScribble</span></span>  <br/> |
|[<span data-ttu-id="91924-120">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="91924-120">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="91924-121">Recursivamente chamar o método **HandsOffMessage** em mensagens inseridas ou o método de OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) nos objetos OLE incorporados.</span><span class="sxs-lookup"><span data-stu-id="91924-121">Recursively invoke the **HandsOffMessage** method on embedded messages or the OLE [IPersistStorage::HandsOffStorage](http://msdn.microsoft.com/library/1e5ef26f-d8e7-4fa6-bfc4-19dace35314d%28Office.15%29.aspx) method on embedded OLE objects.</span></span> <span data-ttu-id="91924-122">Libere o objeto de mensagem e qualquer mensagens inseridas ou objeto.</span><span class="sxs-lookup"><span data-stu-id="91924-122">Release the message object and any embedded messages or objects.</span></span>  <br/> |[<span data-ttu-id="91924-123">HandsOffFromNormal</span><span class="sxs-lookup"><span data-stu-id="91924-123">HandsOffFromNormal</span></span>](handsofffromnormal-state.md) <br/> |
|<span data-ttu-id="91924-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md)</span><span class="sxs-lookup"><span data-stu-id="91924-124">[IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md), [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md)</span></span> <br/> |<span data-ttu-id="91924-125">Defina o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="91924-125">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="91924-126">Normal</span><span class="sxs-lookup"><span data-stu-id="91924-126">Normal</span></span>  <br/> |
|[<span data-ttu-id="91924-127">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="91924-127">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="91924-128">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="91924-128">Return the last error.</span></span>  <br/> |<span data-ttu-id="91924-129">Normal</span><span class="sxs-lookup"><span data-stu-id="91924-129">Normal</span></span>  <br/> |
|<span data-ttu-id="91924-130">Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="91924-130">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="91924-131">Implementar conforme descrito na documentação para o [IPersistMessage: IUnknown](ipersistmessageiunknown.md) interface.</span><span class="sxs-lookup"><span data-stu-id="91924-131">Implement as described in the documentation for the [IPersistMessage : IUnknown](ipersistmessageiunknown.md) interface.</span></span>  <br/> |<span data-ttu-id="91924-132">Normal</span><span class="sxs-lookup"><span data-stu-id="91924-132">Normal</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91924-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="91924-133">See also</span></span>



[<span data-ttu-id="91924-134">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="91924-134">Form States</span></span>](form-states.md)

