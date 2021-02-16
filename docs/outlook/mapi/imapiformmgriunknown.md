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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: fbe6dc9364ee953661d574b70bcd225abcfe7a81
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413056"
---
# <a name="imapiformmgr--iunknown"></a><span data-ttu-id="a6abb-103">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a6abb-103">IMAPIFormMgr : IUnknown</span></span>

  
  
<span data-ttu-id="a6abb-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6abb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6abb-105">Permite que os visualizadores de formulário obtenham informações sobre e ativem servidores de formulário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-105">Enables form viewers to obtain information about and activate form servers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a6abb-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a6abb-106">Header file:</span></span>  <br/> |<span data-ttu-id="a6abb-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="a6abb-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a6abb-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="a6abb-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a6abb-109">Objetos do gerenciador de formulário</span><span class="sxs-lookup"><span data-stu-id="a6abb-109">Form manager objects</span></span>  <br/> |
|<span data-ttu-id="a6abb-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a6abb-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a6abb-111">Provedores de biblioteca de formulário</span><span class="sxs-lookup"><span data-stu-id="a6abb-111">Form library providers</span></span>  <br/> |
|<span data-ttu-id="a6abb-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a6abb-112">Called by:</span></span>  <br/> |<span data-ttu-id="a6abb-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="a6abb-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a6abb-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a6abb-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a6abb-115">IID_IMAPIFormMgr</span><span class="sxs-lookup"><span data-stu-id="a6abb-115">IID_IMAPIFormMgr</span></span>  <br/> |
|<span data-ttu-id="a6abb-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a6abb-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a6abb-117">LPMAPIFORMMGR</span><span class="sxs-lookup"><span data-stu-id="a6abb-117">LPMAPIFORMMGR</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a6abb-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="a6abb-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a6abb-119">LoadForm</span><span class="sxs-lookup"><span data-stu-id="a6abb-119">LoadForm</span></span>](imapiformmgr-loadform.md) <br/> |<span data-ttu-id="a6abb-120">Inicia um formulário para abrir uma mensagem existente.</span><span class="sxs-lookup"><span data-stu-id="a6abb-120">Starts a form to open an existing message.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-121">ResolveMessageClass</span><span class="sxs-lookup"><span data-stu-id="a6abb-121">ResolveMessageClass</span></span>](imapiformmgr-resolvemessageclass.md) <br/> |<span data-ttu-id="a6abb-122">Resolve uma classe de mensagem para seu formulário dentro de um contêiner de formulário e retorna um objeto de informações de formulário para esse formulário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-122">Resolves a message class to its form within a form container, and returns a form information object for that form.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-123">ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="a6abb-123">ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md) <br/> |<span data-ttu-id="a6abb-124">Resolve um grupo de classes de mensagem para seus formulários dentro de um contêiner de formulário e retorna uma matriz de objetos de informações de formulário para esses formulários.</span><span class="sxs-lookup"><span data-stu-id="a6abb-124">Resolves a group of message classes to their forms within a form container, and returns an array of form information objects for those forms.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-125">CalcFormPropSet</span><span class="sxs-lookup"><span data-stu-id="a6abb-125">CalcFormPropSet</span></span>](imapiformmgr-calcformpropset.md) <br/> |<span data-ttu-id="a6abb-126">Retorna uma matriz das propriedades que um grupo de formulários usa.</span><span class="sxs-lookup"><span data-stu-id="a6abb-126">Returns an array of the properties that a group of forms uses.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-127">CreateForm</span><span class="sxs-lookup"><span data-stu-id="a6abb-127">CreateForm</span></span>](imapiformmgr-createform.md) <br/> |<span data-ttu-id="a6abb-128">Inicia um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-128">Launches a form to create a new message based on the form's message class.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-129">SelectForm</span><span class="sxs-lookup"><span data-stu-id="a6abb-129">SelectForm</span></span>](imapiformmgr-selectform.md) <br/> |<span data-ttu-id="a6abb-130">Apresenta uma caixa de diálogo que permite ao usuário selecionar um formulário e retorna um objeto de informações de formulário que descreve esse formulário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-130">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-131">SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="a6abb-131">SelectMultipleForms</span></span>](imapiformmgr-selectmultipleforms.md) <br/> |<span data-ttu-id="a6abb-132">Apresenta uma caixa de diálogo que permite ao usuário selecionar vários formulários e retorna uma matriz de objetos de informações de formulário que descrevem esses formulários.</span><span class="sxs-lookup"><span data-stu-id="a6abb-132">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-133">SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="a6abb-133">SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md) <br/> |<span data-ttu-id="a6abb-134">Apresenta uma caixa de diálogo que permite ao usuário selecionar um contêiner de formulário e retorna uma interface para o objeto contêiner selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-134">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-135">OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="a6abb-135">OpenFormContainer</span></span>](imapiformmgr-openformcontainer.md) <br/> |<span data-ttu-id="a6abb-136">Abre uma [interface IMAPIFormContainer](imapiformcontaineriunknown.md) para um contêiner de formulário específico.</span><span class="sxs-lookup"><span data-stu-id="a6abb-136">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-137">PrepareForm</span><span class="sxs-lookup"><span data-stu-id="a6abb-137">PrepareForm</span></span>](imapiformmgr-prepareform.md) <br/> |<span data-ttu-id="a6abb-138">Baixa um formulário para abertura.</span><span class="sxs-lookup"><span data-stu-id="a6abb-138">Downloads a form for opening.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-139">IsInConflict</span><span class="sxs-lookup"><span data-stu-id="a6abb-139">IsInConflict</span></span>](imapiformmgr-isinconflict.md) <br/> |<span data-ttu-id="a6abb-140">Determina se um formulário pode lidar com seus próprios conflitos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="a6abb-140">Determines whether a form can handle its own message conflicts.</span></span>  <br/> |
|[<span data-ttu-id="a6abb-141">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a6abb-141">GetLastError</span></span>](imapiformmgr-getlasterror.md) <br/> |<span data-ttu-id="a6abb-142">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior ocorrendo no objeto gerenciador de formulário.</span><span class="sxs-lookup"><span data-stu-id="a6abb-142">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form manager object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a6abb-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6abb-143">See also</span></span>



[<span data-ttu-id="a6abb-144">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a6abb-144">MAPI Interfaces</span></span>](mapi-interfaces.md)

