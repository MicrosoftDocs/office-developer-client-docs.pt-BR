---
title: IMAPISupportCopyMessages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CopyMessages
api_type:
- COM
ms.assetid: 70f67614-af0d-43f6-99f6-391a2f5673cb
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 0d3f540a14c833e0ee0ed212f6f3b3b709d72ec0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591034"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="9bfce-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9bfce-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="9bfce-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9bfce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9bfce-105">Cópias ou movimentações de mensagens de uma pasta para outra pasta.</span><span class="sxs-lookup"><span data-stu-id="9bfce-105">Copies or moves messages from one folder to another folder.</span></span>
  
```cpp
HRESULT CopyMessages(
  LPCIID lpSrcInterface,
  LPVOID lpSrcFolder,
  LPENTRYLIST lpMsgList,
  LPCIID lpDestInterface,
  LPVOID lpDestFolder,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="9bfce-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9bfce-106">Parameters</span></span>

 <span data-ttu-id="9bfce-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="9bfce-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="9bfce-108">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a pasta que contém as mensagens devem ser copiados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="9bfce-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="9bfce-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="9bfce-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="9bfce-110">[in] Um ponteiro para a pasta que contém as mensagens devem ser copiados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="9bfce-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="9bfce-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="9bfce-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="9bfce-112">[in] Um ponteiro para uma matriz de identificadores de entrada que identificam as mensagens devem ser copiados ou movidos.</span><span class="sxs-lookup"><span data-stu-id="9bfce-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="9bfce-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="9bfce-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="9bfce-114">[in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar a pasta de destino para as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="9bfce-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="9bfce-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="9bfce-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="9bfce-116">[in] Um ponteiro para a pasta de destino para as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="9bfce-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="9bfce-117">Essa pasta deve ser aberta.</span><span class="sxs-lookup"><span data-stu-id="9bfce-117">This folder must be open.</span></span>
    
 <span data-ttu-id="9bfce-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9bfce-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="9bfce-119">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9bfce-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9bfce-120">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="9bfce-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9bfce-121">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9bfce-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9bfce-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="9bfce-122">_lpProgress_</span></span>
  
> <span data-ttu-id="9bfce-123">[in] Um ponteiro para um objeto de progresso que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9bfce-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="9bfce-124">Se NULL for passado _lpProgress_, o provedor de armazenamento de mensagem exibe um indicador de progresso usando a implementação de objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="9bfce-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="9bfce-125">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG está definido na _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="9bfce-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="9bfce-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9bfce-126">_ulFlags_</span></span>
  
> <span data-ttu-id="9bfce-127">[in] Uma bitmask dos sinalizadores que controla como a operação de cópia ou movimentação é realizada.</span><span class="sxs-lookup"><span data-stu-id="9bfce-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="9bfce-128">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="9bfce-128">The following flags can be set:</span></span>
    
<span data-ttu-id="9bfce-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="9bfce-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="9bfce-130">Solicita a exibição de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9bfce-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="9bfce-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="9bfce-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="9bfce-132">As mensagens devem ser movidas, em vez de copiados.</span><span class="sxs-lookup"><span data-stu-id="9bfce-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="9bfce-133">Se MESSAGE_MOVE não estiver definida, as mensagens serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="9bfce-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9bfce-134">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="9bfce-134">Return value</span></span>

<span data-ttu-id="9bfce-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="9bfce-135">S_OK</span></span> 
  
> <span data-ttu-id="9bfce-136">A operação de cópia ou movimentação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9bfce-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="9bfce-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9bfce-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9bfce-138">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="9bfce-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9bfce-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="9bfce-139">Remarks</span></span>

<span data-ttu-id="9bfce-140">O método **IMAPISupport::CopyMessages** é implementado para objetos de suporte do provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9bfce-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="9bfce-141">Provedores de armazenamento de mensagens podem chamar **IMAPISupport::CopyMessages** na sua implementação do [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) para copiar ou mover uma ou mais mensagens de uma pasta para outro.</span><span class="sxs-lookup"><span data-stu-id="9bfce-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="9bfce-142">Como parte da chamada **IMAPISupport::CopyMessages** , o provedor de armazenamento de mensagens pode especificar que o MAPI deve exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="9bfce-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9bfce-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="9bfce-143">See also</span></span>



[<span data-ttu-id="9bfce-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="9bfce-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="9bfce-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9bfce-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

