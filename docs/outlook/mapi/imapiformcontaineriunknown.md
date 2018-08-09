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
ms.openlocfilehash: 39f255a277403073132dfd3cd21c995eefe904c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767023"
---
# <a name="imapiformcontainer--iunknown"></a><span data-ttu-id="e1728-103">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e1728-103">IMAPIFormContainer : IUnknown</span></span>

  
  
<span data-ttu-id="e1728-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e1728-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e1728-105">Gerencia formulários em bibliotecas de formulários.</span><span class="sxs-lookup"><span data-stu-id="e1728-105">Manages forms in form libraries.</span></span> <span data-ttu-id="e1728-106">Esta interface é usado para criar bibliotecas de formulários do aplicativo específico.</span><span class="sxs-lookup"><span data-stu-id="e1728-106">This interface is used to create application-specific form libraries.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1728-107">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e1728-107">Header file:</span></span>  <br/> |<span data-ttu-id="e1728-108">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="e1728-108">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="e1728-109">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="e1728-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e1728-110">Objetos de contêiner de formulário</span><span class="sxs-lookup"><span data-stu-id="e1728-110">Form container objects</span></span>  <br/> |
|<span data-ttu-id="e1728-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="e1728-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e1728-112">Provedores de biblioteca de formulário</span><span class="sxs-lookup"><span data-stu-id="e1728-112">Form library providers</span></span>  <br/> |
|<span data-ttu-id="e1728-113">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="e1728-113">Called by:</span></span>  <br/> |<span data-ttu-id="e1728-114">Aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="e1728-114">Client applications</span></span>  <br/> |
|<span data-ttu-id="e1728-115">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="e1728-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e1728-116">IID_IMAPIFormContainer</span><span class="sxs-lookup"><span data-stu-id="e1728-116">IID_IMAPIFormContainer</span></span>  <br/> |
|<span data-ttu-id="e1728-117">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="e1728-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e1728-118">LPMAPIFORMCONTAINER</span><span class="sxs-lookup"><span data-stu-id="e1728-118">LPMAPIFORMCONTAINER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e1728-119">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="e1728-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e1728-120">InstallForm</span><span class="sxs-lookup"><span data-stu-id="e1728-120">InstallForm</span></span>](imapiformcontainer-installform.md) <br/> |<span data-ttu-id="e1728-121">Instala um formulário em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-121">Installs a form into a form container.</span></span>  <br/> |
|[<span data-ttu-id="e1728-122">RemoveForm</span><span class="sxs-lookup"><span data-stu-id="e1728-122">RemoveForm</span></span>](imapiformcontainer-removeform.md) <br/> |<span data-ttu-id="e1728-123">Remove um determinado formulário de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-123">Removes a particular form from a form container.</span></span>  <br/> |
|[<span data-ttu-id="e1728-124">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="e1728-124">ResolveMessageClass</span></span>](imapiformcontainer-resolvemessageclass.md) <br/> |<span data-ttu-id="e1728-125">Resolve uma classe de mensagem para o seu formulário em um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-125">Resolves a message class to its form in a form container and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="e1728-126">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e1728-126">ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="e1728-127">Resolve um grupo de classes de mensagens para seus formulários em um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="e1728-127">Resolves a group of message classes to their forms in a form container and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="e1728-128">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="e1728-128">CalcFormPropSet</span></span>](imapiformcontainer-calcformpropset.md) <br/> |<span data-ttu-id="e1728-129">Retorna uma matriz das propriedades usadas por todos os formulários instalados em um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-129">Returns an array of the properties used by all forms installed in a form container.</span></span>  <br/> |
|[<span data-ttu-id="e1728-130">GetDisplay</span><span class="sxs-lookup"><span data-stu-id="e1728-130">GetDisplay</span></span>](imapiformcontainer-getdisplay.md) <br/> |<span data-ttu-id="e1728-131">Retorna o nome de exibição de um contêiner de formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-131">Returns the display name of a form container.</span></span>  <br/> |
|[<span data-ttu-id="e1728-132">GetLastError</span><span class="sxs-lookup"><span data-stu-id="e1728-132">GetLastError</span></span>](imapiformcontainer-getlasterror.md) <br/> |<span data-ttu-id="e1728-133">Retorna uma estrutura [MAPIERROR](mapierror.md) contendo informações sobre o erro anterior que ocorrem ao objeto de contêiner do formulário.</span><span class="sxs-lookup"><span data-stu-id="e1728-133">Returns a [MAPIERROR](mapierror.md) structure containing information about the previous error occurring to the form container object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e1728-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e1728-134">See also</span></span>



[<span data-ttu-id="e1728-135">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="e1728-135">MAPI Interfaces</span></span>](mapi-interfaces.md)

