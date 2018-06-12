---
title: IPersistMessage IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage
api_type:
- COM
ms.assetid: 40ec6dd4-2206-4e59-aafe-53aaf693f973
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 62fb2b069a50408713eea741cf837c421a749fcd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767633"
---
# <a name="ipersistmessage--iunknown"></a><span data-ttu-id="535ac-103">IPersistMessage: IUnknown</span><span class="sxs-lookup"><span data-stu-id="535ac-103">IPersistMessage : IUnknown</span></span>

  
  
<span data-ttu-id="535ac-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="535ac-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="535ac-105">Permite que os visualizadores de formulário lidar com o armazenamento de um formulário e fazer a transição entre os diversos estados.</span><span class="sxs-lookup"><span data-stu-id="535ac-105">Enables form viewers to handle the storage of a form and to transition between the various states.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="535ac-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="535ac-106">Header file:</span></span>  <br/> |<span data-ttu-id="535ac-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="535ac-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="535ac-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="535ac-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="535ac-109">Objetos de mensagem de persistência</span><span class="sxs-lookup"><span data-stu-id="535ac-109">Persist message objects</span></span>  <br/> |
|<span data-ttu-id="535ac-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="535ac-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="535ac-111">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="535ac-111">Form objects</span></span>  <br/> |
|<span data-ttu-id="535ac-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="535ac-112">Called by:</span></span>  <br/> |<span data-ttu-id="535ac-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="535ac-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="535ac-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="535ac-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="535ac-115">IID_IPersistMessage</span><span class="sxs-lookup"><span data-stu-id="535ac-115">IID_IPersistMessage</span></span>  <br/> |
|<span data-ttu-id="535ac-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="535ac-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="535ac-117">LPPERSISTMESSAGE</span><span class="sxs-lookup"><span data-stu-id="535ac-117">LPPERSISTMESSAGE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="535ac-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="535ac-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="535ac-119">GetLastError</span><span class="sxs-lookup"><span data-stu-id="535ac-119">GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="535ac-120">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior no objeto form.</span><span class="sxs-lookup"><span data-stu-id="535ac-120">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error in the form object.</span></span>  <br/> |
|[<span data-ttu-id="535ac-121">GetClassID</span><span class="sxs-lookup"><span data-stu-id="535ac-121">GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="535ac-122">Retorna um identificador que representa o servidor de formulário que pode gerenciar o formulário.</span><span class="sxs-lookup"><span data-stu-id="535ac-122">Returns an identifier that represents the form server that can manage the form.</span></span>  <br/> |
|[<span data-ttu-id="535ac-123">IsDirty</span><span class="sxs-lookup"><span data-stu-id="535ac-123">IsDirty</span></span>](ipersistmessage-isdirty.md) <br/> |<span data-ttu-id="535ac-124">Verifica o formulário para que as alterações feitas desde o último salvamento.</span><span class="sxs-lookup"><span data-stu-id="535ac-124">Checks the form for changes that were made since the last save.</span></span>  <br/> |
|[<span data-ttu-id="535ac-125">InitNew</span><span class="sxs-lookup"><span data-stu-id="535ac-125">InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="535ac-126">Inicializa uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="535ac-126">Initializes a new message.</span></span>  <br/> |
|[<span data-ttu-id="535ac-127">Load</span><span class="sxs-lookup"><span data-stu-id="535ac-127">Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="535ac-128">Carrega o formulário para uma mensagem especificada.</span><span class="sxs-lookup"><span data-stu-id="535ac-128">Loads the form for a specified message.</span></span>  <br/> |
|[<span data-ttu-id="535ac-129">Save</span><span class="sxs-lookup"><span data-stu-id="535ac-129">Save</span></span>](ipersistmessage-save.md) <br/> |<span data-ttu-id="535ac-130">Salva um formulário revisado na mensagem do qual ele foi carregado ou criado.</span><span class="sxs-lookup"><span data-stu-id="535ac-130">Saves a revised form back to the message from which it was loaded or created.</span></span>  <br/> |
|[<span data-ttu-id="535ac-131">SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="535ac-131">SaveCompleted</span></span>](ipersistmessage-savecompleted.md) <br/> |<span data-ttu-id="535ac-132">Notifica o formulário que uma gravação operação foi concluída.</span><span class="sxs-lookup"><span data-stu-id="535ac-132">Notifies the form that a save operation has been completed.</span></span>  <br/> |
|[<span data-ttu-id="535ac-133">HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="535ac-133">HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md) <br/> |<span data-ttu-id="535ac-134">Faz com que o formulário liberar a sua mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="535ac-134">Causes the form to release its current message.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="535ac-135">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="535ac-135">Remarks</span></span>

<span data-ttu-id="535ac-136">Todas as formas são necessários para implementar a interface **IPersistMessage** .</span><span class="sxs-lookup"><span data-stu-id="535ac-136">All forms are required to implement the **IPersistMessage** interface.</span></span> 
  
 <span data-ttu-id="535ac-137">**IPersistMessage** funciona de modo semelhante à interface OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="535ac-137">**IPersistMessage** works similarly to the OLE [IPersistStorage](http://msdn.microsoft.com/library/1c1a20fc-c101-4cbc-a7a6-30613aa387d7%28Office.15%29.aspx) interface.</span></span> <span data-ttu-id="535ac-138">Para obter mais informações, consulte os métodos de **IPersistStorage** .</span><span class="sxs-lookup"><span data-stu-id="535ac-138">For more information, see the **IPersistStorage** methods.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="535ac-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="535ac-139">See also</span></span>



[<span data-ttu-id="535ac-140">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="535ac-140">MAPI Interfaces</span></span>](mapi-interfaces.md)

