---
title: Estado Não Reinicializado
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e071b50f-2e75-4537-ac7b-4a2f5ebea83d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: be35c9d3f8fc7badf83086e63e4c94e0efa4d5bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425558"
---
# <a name="uninitialized-state"></a><span data-ttu-id="aa80e-103">Estado Não Reinicializado</span><span class="sxs-lookup"><span data-stu-id="aa80e-103">Uninitialized State</span></span>

  
  
<span data-ttu-id="aa80e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa80e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="aa80e-105">O estado Não inicializado é o estado inicial em que os objetos de formulário de estado devem estar quando são criados pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="aa80e-105">The Uninitialized state is the initial state form objects should be in when they are first created.</span></span> <span data-ttu-id="aa80e-106">Objetos de formulário são inicializados com dados de mensagem quando um aplicativo cliente chama o método [IPersistMessage::InitNew](ipersistmessage-initnew.md) ou [IPersistMessage::Load](ipersistmessage-load.md) no objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="aa80e-106">Form objects become initialized with message data when a client application calls the [IPersistMessage::InitNew](ipersistmessage-initnew.md) or [IPersistMessage::Load](ipersistmessage-load.md) method on the form object.</span></span> <span data-ttu-id="aa80e-107">A tabela a seguir descreve transições permitidas do estado Unitializado.</span><span class="sxs-lookup"><span data-stu-id="aa80e-107">The following table describes allowed transitions from the Unitialized state.</span></span> 
  
|<span data-ttu-id="aa80e-108">**Método IPersistMessage**</span><span class="sxs-lookup"><span data-stu-id="aa80e-108">**IPersistMessage method**</span></span>|<span data-ttu-id="aa80e-109">**Ação**</span><span class="sxs-lookup"><span data-stu-id="aa80e-109">**Action**</span></span>|<span data-ttu-id="aa80e-110">**Novo estado**</span><span class="sxs-lookup"><span data-stu-id="aa80e-110">**New state**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="aa80e-111">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="aa80e-111">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md) <br/> |<span data-ttu-id="aa80e-112">Carregar o objeto de formulário com dados padrão.</span><span class="sxs-lookup"><span data-stu-id="aa80e-112">Load the form object with default data.</span></span>  <br/> |[<span data-ttu-id="aa80e-113">Normal</span><span class="sxs-lookup"><span data-stu-id="aa80e-113">Normal</span></span>](normal-state.md) <br/> |
|[<span data-ttu-id="aa80e-114">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="aa80e-114">IPersistMessage::Load</span></span>](ipersistmessage-load.md) <br/> |<span data-ttu-id="aa80e-115">Carregue o objeto de formulário com dados da mensagem de destino.</span><span class="sxs-lookup"><span data-stu-id="aa80e-115">Load the form object with data from the target message.</span></span>  <br/> |<span data-ttu-id="aa80e-116">Normal</span><span class="sxs-lookup"><span data-stu-id="aa80e-116">Normal</span></span>  <br/> |
|[<span data-ttu-id="aa80e-117">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="aa80e-117">IPersistMessage::GetClassID</span></span>](ipersistmessage-getclassid.md) <br/> |<span data-ttu-id="aa80e-118">Retornar sucesso ou definir o último erro para e retornar E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="aa80e-118">Return success, or set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="aa80e-119">Não reinicializado</span><span class="sxs-lookup"><span data-stu-id="aa80e-119">Uninitialized</span></span>  <br/> |
|[<span data-ttu-id="aa80e-120">IPersistMessage::GetLastError</span><span class="sxs-lookup"><span data-stu-id="aa80e-120">IPersistMessage::GetLastError</span></span>](ipersistmessage-getlasterror.md) <br/> |<span data-ttu-id="aa80e-121">Retornar o último erro.</span><span class="sxs-lookup"><span data-stu-id="aa80e-121">Return the last error.</span></span>  <br/> |<span data-ttu-id="aa80e-122">Não reinicializado</span><span class="sxs-lookup"><span data-stu-id="aa80e-122">Uninitialized</span></span>  <br/> |
|<span data-ttu-id="aa80e-123">Outros [IPersistMessage : métodos ou métodos IUnknown](ipersistmessageiunknown.md) de outras interfaces</span><span class="sxs-lookup"><span data-stu-id="aa80e-123">Other [IPersistMessage : IUnknown](ipersistmessageiunknown.md) methods or methods from other interfaces</span></span>  <br/> |<span data-ttu-id="aa80e-124">De definida a última mensagem de erro e retorne E_UNEXPECTED.</span><span class="sxs-lookup"><span data-stu-id="aa80e-124">Set the last error to and return E_UNEXPECTED.</span></span>  <br/> |<span data-ttu-id="aa80e-125">Não reinicializado</span><span class="sxs-lookup"><span data-stu-id="aa80e-125">Uninitialized</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aa80e-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa80e-126">See also</span></span>



[<span data-ttu-id="aa80e-127">Estado Normal</span><span class="sxs-lookup"><span data-stu-id="aa80e-127">Normal State</span></span>](normal-state.md)
  
[<span data-ttu-id="aa80e-128">Estados do formulário</span><span class="sxs-lookup"><span data-stu-id="aa80e-128">Form States</span></span>](form-states.md)

