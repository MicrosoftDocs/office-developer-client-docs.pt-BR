---
title: IMAPIFormContainer IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer
api_type:
- COM
ms.assetid: 437c8a75-1121-4919-8bd4-d57c0d6f4b9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 208af28307a60615ecafda0992881c5df36aa56f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407526"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="086d0-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="086d0-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="086d0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="086d0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="086d0-105">Gerencia formulários em bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-105">Manages forms in form libraries.</span></span> <span data-ttu-id="086d0-106">Essa interface é usada para criar bibliotecas de formulários específicas de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="086d0-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="086d0-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="086d0-107">Header file:</span></span>  <br/> |<span data-ttu-id="086d0-108">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="086d0-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="086d0-109">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="086d0-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="086d0-110">Objetos contêiner de formulários</span><span class="sxs-lookup"><span data-stu-id="086d0-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="086d0-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="086d0-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="086d0-112">Provedores de biblioteca de formulários</span><span class="sxs-lookup"><span data-stu-id="086d0-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="086d0-113">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="086d0-113">Called by:</span></span>  <br/> |<span data-ttu-id="086d0-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="086d0-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="086d0-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="086d0-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="086d0-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="086d0-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="086d0-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="086d0-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="086d0-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="086d0-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="086d0-119">Vtable order</span><span class="sxs-lookup"><span data-stu-id="086d0-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="086d0-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="086d0-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="086d0-121">Instala um formulário em um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="086d0-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="086d0-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="086d0-123">Remove um formulário específico de um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="086d0-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="086d0-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="086d0-125">Resolve uma classe de mensagem para seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.</span><span class="sxs-lookup"><span data-stu-id="086d0-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="086d0-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="086d0-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="086d0-127">Resolve um grupo de classes de mensagem para seus formulários em um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="086d0-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="086d0-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="086d0-129">Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="086d0-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="086d0-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="086d0-131">Retorna o nome de exibição de um contêiner de formulários.</span><span class="sxs-lookup"><span data-stu-id="086d0-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="086d0-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="086d0-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="086d0-133">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="086d0-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="086d0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="086d0-134">See also</span></span>



[<span data-ttu-id="086d0-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="086d0-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

