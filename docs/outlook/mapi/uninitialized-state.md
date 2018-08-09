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
ms.openlocfilehash: c00d5bb2e5da02b007579c7a8206baa98f64143f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770656"
---
# <a name="uninitialized-state"></a><span data-ttu-id="dbada-103">Estado Uninitialized</span><span class="sxs-lookup"><span data-stu-id="dbada-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="dbada-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dbada-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dbada-105">O estado não inicializado é o formulário de estado inicial objetos devem estar no quando forem criados pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="dbada-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="dbada-106">Objetos de formulário se tornam inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) no objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="dbada-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="dbada-107">A tabela a seguir descreve as transições permitidas do estado de Unitialized.</span><span class="sxs-lookup"><span data-stu-id="dbada-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="dbada-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="dbada-108">**IPersistMessage method**</span></span>|<span data-ttu-id="dbada-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="dbada-109">**Action**</span></span>|<span data-ttu-id="dbada-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="dbada-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="dbada-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="dbada-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="dbada-112">Carregar o objeto de formulário com os dados padrão.</span><span class="sxs-lookup"><span data-stu-id="dbada-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="dbada-113">Normal</span><span class="sxs-lookup"><span data-stu-id="dbada-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="dbada-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="dbada-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="dbada-115">Carregar o objeto de formulário com os dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="dbada-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="dbada-116">Normal</span><span class="sxs-lookup"><span data-stu-id="dbada-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="dbada-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="dbada-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="dbada-118">Retornar o sucesso, ou definir o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="dbada-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="dbada-119">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="dbada-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="dbada-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="dbada-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="dbada-121">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="dbada-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="dbada-122">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="dbada-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="dbada-123">Outros [IPersistMessage: IUnknown](ipersistmessageiunknown.md) métodos ou métodos de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="dbada-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="dbada-124">Defina o último erro como e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="dbada-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="dbada-125">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="dbada-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbada-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="dbada-126">See also</span></span>



[<span data-ttu-id="dbada-127">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="dbada-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="dbada-128">Estados de formulários</span><span class="sxs-lookup"><span data-stu-id="dbada-128">Form States</span></span>](form-states.md)

