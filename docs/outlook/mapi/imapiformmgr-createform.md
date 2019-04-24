---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321662"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="0d483-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="0d483-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="0d483-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0d483-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0d483-105">Abre um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="0d483-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="0d483-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d483-106">Parameters</span></span>

 <span data-ttu-id="0d483-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0d483-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0d483-108">no Uma alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="0d483-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="0d483-109">O parâmetro _ulUIParam_ é ignorado, a menos que o sinalizador MAPI_DIALOG esteja definido no parâmetro _parâmetroulflags_ .</span><span class="sxs-lookup"><span data-stu-id="0d483-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0d483-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0d483-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0d483-111">no Uma bitmask de sinalizadores que controla como o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="0d483-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="0d483-112">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="0d483-112">The following flag can be set:</span></span>
    
<span data-ttu-id="0d483-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0d483-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0d483-114">Exibe uma interface do usuário para fornecer status ou solicitar mais informações ao usuário.</span><span class="sxs-lookup"><span data-stu-id="0d483-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="0d483-115">Se esse sinalizador não for definido, nenhuma interface de usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="0d483-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="0d483-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="0d483-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="0d483-117">no Um ponteiro para o objeto de informações do formulário que é usado para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="0d483-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="0d483-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="0d483-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="0d483-119">no Um ponteiro para o identificador de interface (IID) da interface a ser retornado para o objeto Form que foi criado.</span><span class="sxs-lookup"><span data-stu-id="0d483-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="0d483-120">O parâmetro _refiidToAsk_ não deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="0d483-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="0d483-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="0d483-121">_ppvObj_</span></span>
  
> <span data-ttu-id="0d483-122">bota Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="0d483-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0d483-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0d483-123">Return value</span></span>

<span data-ttu-id="0d483-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0d483-124">S_OK</span></span> 
  
> <span data-ttu-id="0d483-125">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="0d483-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0d483-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="0d483-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="0d483-127">A interface solicitada não é suportada pelo objeto Form.</span><span class="sxs-lookup"><span data-stu-id="0d483-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0d483-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d483-128">Remarks</span></span>

<span data-ttu-id="0d483-129">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: CreateForm** para abrir um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="0d483-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="0d483-130">**CreateForm** abre o formulário criando uma instância do servidor de formulário para esse formulário, conforme descrito no objeto de informações do formulário determinado.</span><span class="sxs-lookup"><span data-stu-id="0d483-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="0d483-131">Se necessário, **CreateForm** chama o método [IMAPIFormMgr::P repareform](imapiformmgr-prepareform.md) para baixar o código do servidor de formulário no disco do usuário.</span><span class="sxs-lookup"><span data-stu-id="0d483-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="0d483-132">O parâmetro _pfrminfoToActivate_ deve apontar para um objeto de informações de formulário que foi resolvido corretamente.</span><span class="sxs-lookup"><span data-stu-id="0d483-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="0d483-133">Depois que o formulário é aberto, o Visualizador de formulário de chamada deve configurar uma mensagem usando a interface [IPersistMessage](ipersistmessageiunknown.md) e, opcionalmente, pode configurar um contexto de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="0d483-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="0d483-134">Para obter mais informações, consulte [iniciando um servidor de formulários](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="0d483-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0d483-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0d483-135">MFCMAPI reference</span></span>

<span data-ttu-id="0d483-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0d483-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0d483-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="0d483-137">**File**</span></span>|<span data-ttu-id="0d483-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="0d483-138">**Function**</span></span>|<span data-ttu-id="0d483-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="0d483-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0d483-140">MAPIFormFunctions. cpp</span><span class="sxs-lookup"><span data-stu-id="0d483-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0d483-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="0d483-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="0d483-142">MFCMAPI usa o método **IMAPIFormMgr:: CreateForm** para criar um formulário antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="0d483-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d483-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0d483-143">See also</span></span>



[<span data-ttu-id="0d483-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="0d483-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="0d483-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d483-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="0d483-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0d483-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="0d483-147">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="0d483-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0d483-148">Iniciar um servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="0d483-148">Launching a Form Server</span></span>](launching-a-form-server.md)

