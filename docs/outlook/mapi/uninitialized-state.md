---
title: Estado Uninitialized
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 95ed80a6d0ea6a6a7c8cc768b32981ac899b69e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578245"
---
# <a name="uninitialized-state"></a><span data-ttu-id="df985-103">Estado Uninitialized</span><span class="sxs-lookup"><span data-stu-id="df985-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="df985-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df985-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df985-105">O estado não inicializado é o formulário de estado inicial objetos devem estar no quando forem criados pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="df985-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="df985-106">Objetos de formulário se tornam inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) no objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="df985-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="df985-107">A tabela a seguir descreve as transições permitidas do estado de Unitialized.</span><span class="sxs-lookup"><span data-stu-id="df985-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="df985-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="df985-108">**IPersistMessage method**</span></span>|<span data-ttu-id="df985-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="df985-109">**Action**</span></span>|<span data-ttu-id="df985-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="df985-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="df985-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="df985-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="df985-112">Carregar o objeto de formulário com os dados padrão.</span><span class="sxs-lookup"><span data-stu-id="df985-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="df985-113">Normal</span><span class="sxs-lookup"><span data-stu-id="df985-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="df985-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="df985-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="df985-115">Carregar o objeto de formulário com os dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="df985-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="df985-116">Normal</span><span class="sxs-lookup"><span data-stu-id="df985-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="df985-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="df985-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="df985-118">Retornar o sucesso, ou definir o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="df985-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="df985-119">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="df985-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="df985-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="df985-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="df985-121">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="df985-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="df985-122">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="df985-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="df985-123">Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="df985-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="df985-124">Defina o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="df985-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="df985-125">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="df985-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df985-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="df985-126">See also</span></span>



[<span data-ttu-id="df985-127">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="df985-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="df985-128">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="df985-128">Form States</span></span>](form-states.md)

