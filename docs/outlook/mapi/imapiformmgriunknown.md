---
title: IMAPIFormMgr IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr
api_type:
- COM
ms.assetid: 8cbd1a42-7de6-43e0-8c77-7711773843d5
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 4fdd50a1108a6546445516664b01fb0f994fbfdb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767066"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="db7c3-103">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="db7c3-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="db7c3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="db7c3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="db7c3-105">Permite que os visualizadores de formulário obter informações sobre e ativar servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="db7c3-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db7c3-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="db7c3-106">Header file:</span></span>  <br/> |<span data-ttu-id="db7c3-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="db7c3-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="db7c3-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="db7c3-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="db7c3-109">Objetos de Gerenciador de formulário</span><span class="sxs-lookup"><span data-stu-id="db7c3-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="db7c3-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="db7c3-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="db7c3-111">Provedores de biblioteca de formulário</span><span class="sxs-lookup"><span data-stu-id="db7c3-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="db7c3-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="db7c3-112">Called by:</span></span>  <br/> |<span data-ttu-id="db7c3-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="db7c3-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="db7c3-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="db7c3-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="db7c3-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="db7c3-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="db7c3-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="db7c3-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="db7c3-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="db7c3-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="db7c3-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="db7c3-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="db7c3-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="db7c3-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="db7c3-120">Inicia um formulário para abrir uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="db7c3-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="db7c3-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="db7c3-122">Resolve uma classe de mensagem para o seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="db7c3-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="db7c3-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="db7c3-124">Resolve um grupo de classes de mensagens para seus formulários dentro de um contêiner de formulário e retorna uma matriz de formulário objetos de informações para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="db7c3-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="db7c3-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="db7c3-126">Retorna uma matriz das propriedades que usa um grupo de formulários.</span><span class="sxs-lookup"><span data-stu-id="db7c3-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="db7c3-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="db7c3-128">Inicia um formulário para criar uma nova mensagem, com base na classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="db7c3-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="db7c3-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="db7c3-130">Apresenta uma caixa de diálogo que permite que o usuário selecione um formulário e retorna um objeto de informações de formulário que descreve nesse formulário.</span><span class="sxs-lookup"><span data-stu-id="db7c3-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="db7c3-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="db7c3-132">Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de formulário objetos de informações que descrevem esses formulários.</span><span class="sxs-lookup"><span data-stu-id="db7c3-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="db7c3-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="db7c3-134">Apresenta uma caixa de diálogo que permite que o usuário selecione um contêiner de formulário e retorna uma interface para o objeto de contêiner do usuário selecionado.</span><span class="sxs-lookup"><span data-stu-id="db7c3-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="db7c3-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="db7c3-136">Abre uma interface [IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="db7c3-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="db7c3-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="db7c3-138">Baixa um formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="db7c3-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="db7c3-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="db7c3-140">Determina se um formulário pode lidar com conflitos sua própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="db7c3-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="db7c3-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="db7c3-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="db7c3-142">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form manager.</span><span class="sxs-lookup"><span data-stu-id="db7c3-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db7c3-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="db7c3-143">See also</span></span>



[<span data-ttu-id="db7c3-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="db7c3-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

