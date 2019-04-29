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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 87432d8982c5dc1f64396187739e97314edb385c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412881"
---
# <a name="imapiformmgrisinconflict"></a><span data-ttu-id="1add4-103">IMAPIFormMgr::IsInConflict</span><span class="sxs-lookup"><span data-stu-id="1add4-103">IMAPIFormMgr::IsInConflict</span></span>

  
  
<span data-ttu-id="1add4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1add4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1add4-105">Determina se um formulário pode lidar com seus próprios conflitos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-105">Determines whether a form can handle its own message conflicts.</span></span> <span data-ttu-id="1add4-106">Uma mensagem estará em conflito se tiver sido editada simultaneamente por mais de um usuário.</span><span class="sxs-lookup"><span data-stu-id="1add4-106">A message is in conflict if it has been simultaneously edited by more than one user.</span></span> <span data-ttu-id="1add4-107">Isso pode acontecer com mensagens em pastas públicas.</span><span class="sxs-lookup"><span data-stu-id="1add4-107">This can happen to messages in public folders.</span></span>
  
```cpp
HRESULT IsInConflict(
  ULONG ulMessageFlags,
  ULONG ulMessageStatus,
  LPCSTR szMessageClass LPMAPIFOLDER pFolderFocus
);
```

## <a name="parameters"></a><span data-ttu-id="1add4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1add4-108">Parameters</span></span>

 <span data-ttu-id="1add4-109">_ulMessageFlags_</span><span class="sxs-lookup"><span data-stu-id="1add4-109">_ulMessageFlags_</span></span>
  
> <span data-ttu-id="1add4-110">no Um ponteiro para uma bitmask de sinalizadores copiados da propriedade **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) de uma mensagem que indica o estado atual da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-110">[in] A pointer to a bitmask of flags copied from the **PR_MESSAGE_FLAGS** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md)) property of a message that indicates the current state of the message.</span></span>
    
 <span data-ttu-id="1add4-111">_ulMessageStatus_</span><span class="sxs-lookup"><span data-stu-id="1add4-111">_ulMessageStatus_</span></span>
  
> <span data-ttu-id="1add4-112">no Uma bitmask de sinalizadores definidos pelo cliente ou definidos pelo provedor copiados da propriedade **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) de uma mensagem que fornece informações adicionais sobre o estado da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-112">[in] A bitmask of client-defined or provider-defined flags copied from the **PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) property of a message that provides additional information about the state of the message.</span></span>
    
 <span data-ttu-id="1add4-113">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="1add4-113">_szMessageClass_</span></span>
  
> <span data-ttu-id="1add4-114">no Uma cadeia de caracteres que nomeia a classe de mensagem da mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-114">[in] A string that names the message's message class.</span></span>
    
 <span data-ttu-id="1add4-115">_pFolderFocus_</span><span class="sxs-lookup"><span data-stu-id="1add4-115">_pFolderFocus_</span></span>
  
> <span data-ttu-id="1add4-116">no Um ponteiro para a pasta que contém a mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-116">[in] A pointer to the folder that contains the message.</span></span> <span data-ttu-id="1add4-117">O parâmetro _pFolderFocus_ pode ser NULL se essa pasta não existir (por exemplo, se a mensagem estiver incorporada a outra mensagem).</span><span class="sxs-lookup"><span data-stu-id="1add4-117">The  _pFolderFocus_ parameter can be NULL if such a folder does not exist (for example, if the message is embedded in another message).</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1add4-118">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1add4-118">Return value</span></span>

<span data-ttu-id="1add4-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1add4-119">S_OK</span></span> 
  
> <span data-ttu-id="1add4-120">O formulário não manipula seus próprios conflitos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-120">The form does not handle its own message conflicts.</span></span>
    
<span data-ttu-id="1add4-121">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="1add4-121">S_FALSE</span></span> 
  
> <span data-ttu-id="1add4-122">O formulário manipula seus próprios conflitos de mensagem ou a mensagem para a qual as informações foram transmitidas não está em conflito.</span><span class="sxs-lookup"><span data-stu-id="1add4-122">The form handles its own message conflicts, or the message for which information was passed is not in conflict.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1add4-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1add4-123">Remarks</span></span>

<span data-ttu-id="1add4-124">Os visualizadores de formulários chamam o método **IMAPIFormMgr:: IsInConflict** para descobrir se um determinado formulário não manipula seus próprios conflitos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="1add4-124">Form viewers call the **IMAPIFormMgr::IsInConflict** method to discover whether a particular form does not handle its own message conflicts.</span></span> <span data-ttu-id="1add4-125">**IsInConflict** verifica os bitmasks nos parâmetros _ulMessageFlags_ e _ulMessageStatus_ para a presença de um sinalizador de conflito.</span><span class="sxs-lookup"><span data-stu-id="1add4-125">**IsInConflict** checks the bitmasks in the  _ulMessageFlags_ and  _ulMessageStatus_ parameters for the presence of a conflict flag.</span></span> <span data-ttu-id="1add4-126">Se um sinalizador de conflito estiver definido, **IsInConflict** resolverá a classe de mensagem passada no parâmetro _SZMESSAGECLASS_ e retornará S_OK se o formulário não manipular seus próprios conflitos.</span><span class="sxs-lookup"><span data-stu-id="1add4-126">If a conflict flag is set, **IsInConflict** resolves the message class passed in the  _szMessageClass_ parameter and returns S_OK if the form does not handle its own conflicts.</span></span> <span data-ttu-id="1add4-127">**IsInConflict** retornará S_FALSE se o formulário manipular seus próprios conflitos.</span><span class="sxs-lookup"><span data-stu-id="1add4-127">**IsInConflict** returns S_FALSE if the form handles its own conflicts.</span></span> 
  
<span data-ttu-id="1add4-128">Um formulário que não manipula seus próprios conflitos deve ser aberto usando o método [IMAPIFormMgr:: loadform](imapiformmgr-loadform.md) e não pode reutilizar um objeto Form existente.</span><span class="sxs-lookup"><span data-stu-id="1add4-128">A form that does not handle its own conflicts must be opened by using the [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) method and cannot reuse an existing form object.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1add4-129">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="1add4-129">Notes to callers</span></span>

<span data-ttu-id="1add4-130">Os aplicativos clientes normalmente precisam lidar com conflitos quando os aplicativos são movidos de uma mensagem para a mensagem seguinte ou anterior em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="1add4-130">Client applications typically have to deal with conflicts when the applications move from one message to the next or previous message in a folder.</span></span> <span data-ttu-id="1add4-131">Se uma mensagem estiver em conflito, mas o servidor de formulário dessa mensagem puder lidar com conflitos, o aplicativo cliente deverá executar o código habitual para exibir a mensagem seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="1add4-131">If a message is in conflict, but the form server for that message can handle conflicts, the client application should execute its usual code for displaying the next or previous message.</span></span> <span data-ttu-id="1add4-132">Se o servidor de formulário não puder lidar com conflitos, o aplicativo cliente deve continuar como se não estivesse ciente da classe de mensagem da mensagem seguinte ou anterior.</span><span class="sxs-lookup"><span data-stu-id="1add4-132">If the form server cannot handle conflicts, the client application should continue as if it was unaware of the message class of the next or previous message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1add4-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="1add4-133">See also</span></span>



[<span data-ttu-id="1add4-134">IMAPIFormAdviseSink::OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="1add4-134">IMAPIFormAdviseSink::OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md)
  
[<span data-ttu-id="1add4-135">Propriedade canônica PidTagMessageFlags</span><span class="sxs-lookup"><span data-stu-id="1add4-135">PidTagMessageFlags Canonical Property</span></span>](pidtagmessageflags-canonical-property.md)
  
[<span data-ttu-id="1add4-136">Propriedade canônica PidTagMessageStatus</span><span class="sxs-lookup"><span data-stu-id="1add4-136">PidTagMessageStatus Canonical Property</span></span>](pidtagmessagestatus-canonical-property.md)
  
[<span data-ttu-id="1add4-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1add4-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

