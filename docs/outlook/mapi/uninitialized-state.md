---
title: Estado não inicializado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360498"
---
# <a name="uninitialized-state"></a><span data-ttu-id="6edeb-103">Estado não inicializado</span><span class="sxs-lookup"><span data-stu-id="6edeb-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="6edeb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6edeb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6edeb-105">O estado não inicializado é o objeto de formulário de estado inicial que deve ser quando criados pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="6edeb-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="6edeb-106">Os objetos Form são inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage:: InitNew](ipersistmessage-initnew.md) ou [IPersistMessage:: Load](ipersistmessage-load.md) no objeto Form.</span><span class="sxs-lookup"><span data-stu-id="6edeb-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="6edeb-107">A tabela a seguir descreve as transições permitidas do estado unitialized.</span><span class="sxs-lookup"><span data-stu-id="6edeb-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="6edeb-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="6edeb-108">**IPersistMessage method**</span></span>|<span data-ttu-id="6edeb-109">**Action**</span><span class="sxs-lookup"><span data-stu-id="6edeb-109">**Action**</span></span>|<span data-ttu-id="6edeb-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="6edeb-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6edeb-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="6edeb-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="6edeb-112">Carregar o objeto Form com dados padrão.</span><span class="sxs-lookup"><span data-stu-id="6edeb-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="6edeb-113">Normal</span><span class="sxs-lookup"><span data-stu-id="6edeb-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="6edeb-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6edeb-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="6edeb-115">Carregar o objeto Form com dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="6edeb-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="6edeb-116">Normal</span><span class="sxs-lookup"><span data-stu-id="6edeb-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="6edeb-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="6edeb-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="6edeb-118">Retornar êxito ou definir o último erro para e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="6edeb-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="6edeb-119">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="6edeb-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="6edeb-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="6edeb-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="6edeb-121">Retorna o último erro.</span><span class="sxs-lookup"><span data-stu-id="6edeb-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="6edeb-122">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="6edeb-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="6edeb-123">Outros métodos [IPersistMessage: IUnknown](ipersistmessageiunknown.md) de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="6edeb-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="6edeb-124">Definir o último erro para e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="6edeb-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="6edeb-125">Não inicializado</span><span class="sxs-lookup"><span data-stu-id="6edeb-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6edeb-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6edeb-126">See also</span></span>



[<span data-ttu-id="6edeb-127">Estado normal</span><span class="sxs-lookup"><span data-stu-id="6edeb-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="6edeb-128">Estados de formulário</span><span class="sxs-lookup"><span data-stu-id="6edeb-128">Form States</span></span>](form-states.md)

