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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419846"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="fd3c7-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="fd3c7-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="fd3c7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fd3c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fd3c7-105">Abre um formulário para criar uma nova mensagem com base na classe de mensagem do formulário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="fd3c7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd3c7-106">Parameters</span></span>

 <span data-ttu-id="fd3c7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="fd3c7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="fd3c7-108">[in] Um alça para a janela pai do indicador de progresso que é exibido enquanto o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="fd3c7-109">O _parâmetro ulUIParam é_ ignorado, a menos que o MAPI_DIALOG padrão seja definido no parâmetro _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="fd3c7-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="fd3c7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fd3c7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fd3c7-111">[in] Uma máscara de bits de sinalizadores que controla como o formulário é aberto.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="fd3c7-112">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="fd3c7-112">The following flag can be set:</span></span>
    
<span data-ttu-id="fd3c7-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="fd3c7-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="fd3c7-114">Exibe uma interface do usuário para fornecer status ou solicitar ao usuário mais informações.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="fd3c7-115">Se esse sinalizador não estiver definido, nenhuma interface do usuário será exibida.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="fd3c7-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="fd3c7-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="fd3c7-117">[in] Um ponteiro para o objeto de informações de formulário que é usado para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="fd3c7-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="fd3c7-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="fd3c7-119">[in] Um ponteiro para o identificador de interface (IID) para a interface a ser retornada para o objeto de formulário que foi criado.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="fd3c7-120">O  _parâmetro refiidToAsk_ não deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="fd3c7-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="fd3c7-121">_ppvObj_</span></span>
  
> <span data-ttu-id="fd3c7-122">[out] Um ponteiro para um ponteiro para a interface retornada.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fd3c7-123">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fd3c7-123">Return value</span></span>

<span data-ttu-id="fd3c7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="fd3c7-124">S_OK</span></span> 
  
> <span data-ttu-id="fd3c7-125">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fd3c7-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="fd3c7-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="fd3c7-127">A interface solicitada não é suportada pelo objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fd3c7-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd3c7-128">Remarks</span></span>

<span data-ttu-id="fd3c7-129">Visualizadores de formulário chamam o método **IMAPIFormMgr::CreateForm** para abrir um formulário e criar uma nova mensagem com base na classe de mensagens do formulário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="fd3c7-130">**CreateForm** abre o formulário criando uma instância do servidor de formulário para esse formulário, conforme descrito no objeto de informações do formulário determinado.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="fd3c7-131">Se necessário, **CreateForm** chama o [método IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) para baixar o código do servidor de formulário no disco do usuário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="fd3c7-132">O  _parâmetro pfrminfoToActivate_ deve apontar para um objeto de informação de formulário que tenha sido resolvido corretamente.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="fd3c7-133">Depois que o formulário tiver sido aberto, o visualizador de formulário de chamada deverá configurar uma mensagem usando a interface [IPersistMessage](ipersistmessageiunknown.md) e, opcionalmente, poderá configurar um contexto de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="fd3c7-134">Para obter mais informações, consulte [Iniciando um servidor de formulário.](launching-a-form-server.md)</span><span class="sxs-lookup"><span data-stu-id="fd3c7-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fd3c7-135">Referência do MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fd3c7-135">MFCMAPI reference</span></span>

<span data-ttu-id="fd3c7-136">Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fd3c7-137">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="fd3c7-137">**File**</span></span>|<span data-ttu-id="fd3c7-138">**Função**</span><span class="sxs-lookup"><span data-stu-id="fd3c7-138">**Function**</span></span>|<span data-ttu-id="fd3c7-139">**Comentário**</span><span class="sxs-lookup"><span data-stu-id="fd3c7-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fd3c7-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="fd3c7-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="fd3c7-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="fd3c7-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="fd3c7-142">MFCMAPI usa o **método IMAPIFormMgr::CreateForm** para criar um formulário antes de exibi-lo.</span><span class="sxs-lookup"><span data-stu-id="fd3c7-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd3c7-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="fd3c7-143">See also</span></span>



[<span data-ttu-id="fd3c7-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="fd3c7-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="fd3c7-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd3c7-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="fd3c7-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fd3c7-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="fd3c7-147">MFCMAPI como exemplo de código</span><span class="sxs-lookup"><span data-stu-id="fd3c7-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="fd3c7-148">Iniciando um servidor de formulário</span><span class="sxs-lookup"><span data-stu-id="fd3c7-148">Launching a Form Server</span></span>](launching-a-form-server.md)

