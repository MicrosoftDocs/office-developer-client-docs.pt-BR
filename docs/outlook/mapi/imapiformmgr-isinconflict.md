---
title: IMAPIFormMgrIsInConflict
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgrIsInConflict
api_type:
- COM
ms.assetid: 5ca86ee8-1bf6-4ec8-95b3-575c22fbb170
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: d8f28a6b0a1633b0060f02af7e38ef058527eb24
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767042"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="f954e-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="f954e-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="f954e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f954e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f954e-105">Determina se um formulário pode lidar com conflitos sua própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="f954e-106">Uma mensagem está em conflito se ele tiver sido editado simultaneamente por mais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="f954e-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="f954e-107">Isso pode acontecer às mensagens em pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="f954e-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="f954e-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f954e-108">Parameters</span></span>

 <span data-ttu-id="f954e-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="f954e-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="f954e-110">[in] Um ponteiro para uma bitmask dos sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma mensagem que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="f954e-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="f954e-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="f954e-112">[in] Uma bitmask dos sinalizadores definido pelo provedor ou cliente copiado da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de uma mensagem que fornece informações adicionais sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="f954e-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="f954e-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="f954e-114">[in] Uma cadeia de caracteres que nomeia a classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="f954e-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="f954e-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="f954e-116">[in] Um ponteiro para a pasta que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="f954e-117">O parâmetro _pFolderFocus_ pode ser NULL se tal uma pasta não existir (por exemplo, se a mensagem é incorporada em outra mensagem).</span><span class="sxs-lookup"><span data-stu-id="f954e-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f954e-118">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f954e-118">Return value</span></span>

<span data-ttu-id="f954e-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="f954e-119">S_OK</span></span> 
  
> <span data-ttu-id="f954e-120">O formulário não lidar com conflitos sua própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="f954e-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="f954e-121">S_FALSE</span></span> 
  
> <span data-ttu-id="f954e-122">O formulário manipula conflitos sua própria mensagem ou a mensagem para os quais informações passadas não está em conflito.</span><span class="sxs-lookup"><span data-stu-id="f954e-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f954e-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f954e-123">Remarks</span></span>

<span data-ttu-id="f954e-124">Visualizadores de formulário chame o método de **IMAPIFormMgr::IsInConflict** para descobrir se a determinado formulário não lidar com conflitos sua própria mensagem.</span><span class="sxs-lookup"><span data-stu-id="f954e-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="f954e-125">**IsInConflict** verifica a bitmasks nos parâmetros _ulMessageFlags_ e _ulMessageStatus_ a presença de um sinalizador de conflito.</span><span class="sxs-lookup"><span data-stu-id="f954e-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="f954e-126">Se for definido um sinalizador de conflito, **IsInConflict** resolva a classe de mensagem passada no parâmetro _szMessageClass_ e retorna S_OK se o formulário não manipular seus próprio conflitos.</span><span class="sxs-lookup"><span data-stu-id="f954e-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="f954e-127">**IsInConflict** retorna S_FALSE se o formulário manipula o seus próprio conflitos.</span><span class="sxs-lookup"><span data-stu-id="f954e-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="f954e-128">Um formulário que não lidar com seus próprio conflitos deve ser aberto usando o método [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) e não pode reutilizar um objeto de formulário existente.</span><span class="sxs-lookup"><span data-stu-id="f954e-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f954e-129">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f954e-129">Notes to callers</span></span>

<span data-ttu-id="f954e-130">Aplicativos clientes geralmente têm que lidar com conflitos quando os aplicativos se move de uma mensagem para a mensagem anterior ou seguinte em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="f954e-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="f954e-131">Se uma mensagem está em conflito, mas o servidor de formulário para essa mensagem pode lidar com conflitos, o aplicativo cliente deve executar o seu código usual para exibir a mensagem anterior ou seguinte.</span><span class="sxs-lookup"><span data-stu-id="f954e-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="f954e-132">Se o servidor de formulário não pode lidar com conflitos, o aplicativo cliente deve continuar como se fosse não sabem da classe de mensagem da mensagem seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="f954e-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f954e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f954e-133">See also</span></span>



[<span data-ttu-id="f954e-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="f954e-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="f954e-135">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="f954e-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="f954e-136">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="f954e-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="f954e-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f954e-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

