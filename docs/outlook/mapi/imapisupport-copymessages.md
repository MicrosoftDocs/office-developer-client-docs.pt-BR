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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9cc4e3ba77395e09a6b95e8381fa402fc3cdff61
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405153"
---
# <a name="imapisupportcopymessages"></a><span data-ttu-id="2bbe1-103">IMAPISupport::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="2bbe1-103">IMAPISupport::CopyMessages</span></span>

  
  
<span data-ttu-id="2bbe1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2bbe1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2bbe1-105">Copia ou move mensagens de uma pasta para outra.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-105">Copies or moves messages from one folder to another folder.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="2bbe1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2bbe1-106">Parameters</span></span>

 <span data-ttu-id="2bbe1-107">_lpSrcInterface_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-107">_lpSrcInterface_</span></span>
  
> <span data-ttu-id="2bbe1-108">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta que contém as mensagens a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="2bbe1-109">_lpSrcFolder_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-109">_lpSrcFolder_</span></span>
  
> <span data-ttu-id="2bbe1-110">no Um ponteiro para a pasta que contém as mensagens a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-110">[in] A pointer to the folder that contains the messages to be copied or moved.</span></span>
    
 <span data-ttu-id="2bbe1-111">_lpMsgList_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-111">_lpMsgList_</span></span>
  
> <span data-ttu-id="2bbe1-112">no Um ponteiro para uma matriz de identificadores de entrada que identificam as mensagens a serem copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-112">[in] A pointer to an array of entry identifiers that identify the messages to be copied or moved.</span></span> 
    
 <span data-ttu-id="2bbe1-113">_lpDestInterface_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-113">_lpDestInterface_</span></span>
  
> <span data-ttu-id="2bbe1-114">no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a pasta de destino para as mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-114">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the destination folder for the copied or moved messages.</span></span>
    
 <span data-ttu-id="2bbe1-115">_lpDestFolder_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-115">_lpDestFolder_</span></span>
  
> <span data-ttu-id="2bbe1-116">no Um ponteiro para a pasta de destino das mensagens copiadas ou movidas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-116">[in] A pointer to the destination folder for the copied or moved messages.</span></span> <span data-ttu-id="2bbe1-117">Essa pasta deve ser aberta.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-117">This folder must be open.</span></span>
    
 <span data-ttu-id="2bbe1-118">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-118">_ulUIParam_</span></span>
  
> <span data-ttu-id="2bbe1-119">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-119">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2bbe1-120">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-120">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2bbe1-121">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-121">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2bbe1-122">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-122">_lpProgress_</span></span>
  
> <span data-ttu-id="2bbe1-123">no Um ponteiro para um objeto Progress que exibe um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-123">[in] A pointer to a progress object that displays a progress indicator.</span></span> <span data-ttu-id="2bbe1-124">Se NULL for passado no _lpProgress_, o provedor de armazenamento de mensagens exibirá um indicador de progresso usando a implementação do objeto de progresso MAPI.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-124">If NULL is passed in  _lpProgress_, the message store provider displays a progress indicator by using the MAPI progress object implementation.</span></span> <span data-ttu-id="2bbe1-125">O parâmetro _lpProgress_ é ignorado, a menos que o sinalizador MESSAGE_DIALOG esteja definido em _parâmetroulflags_.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-125">The  _lpProgress_ parameter is ignored unless the MESSAGE_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="2bbe1-126">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2bbe1-126">_ulFlags_</span></span>
  
> <span data-ttu-id="2bbe1-127">no Uma bitmask de sinalizadores que controlam como a operação de cópia ou movimentação é realizada.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-127">[in] A bitmask of flags that controls how the copy or move operation is accomplished.</span></span> <span data-ttu-id="2bbe1-128">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="2bbe1-128">The following flags can be set:</span></span>
    
<span data-ttu-id="2bbe1-129">MESSAGE_DIALOG</span><span class="sxs-lookup"><span data-stu-id="2bbe1-129">MESSAGE_DIALOG</span></span> 
  
> <span data-ttu-id="2bbe1-130">Solicita a exibição de um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-130">Requests the display of a progress indicator.</span></span>
    
<span data-ttu-id="2bbe1-131">MESSAGE_MOVE</span><span class="sxs-lookup"><span data-stu-id="2bbe1-131">MESSAGE_MOVE</span></span> 
  
> <span data-ttu-id="2bbe1-132">As mensagens devem ser movidas, em vez de copiadas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-132">The messages should be moved, instead of copied.</span></span> <span data-ttu-id="2bbe1-133">Se MESSAGE_MOVE não for definido, as mensagens serão copiadas.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-133">If MESSAGE_MOVE is not set, the messages are copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2bbe1-134">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2bbe1-134">Return value</span></span>

<span data-ttu-id="2bbe1-135">S_OK</span><span class="sxs-lookup"><span data-stu-id="2bbe1-135">S_OK</span></span> 
  
> <span data-ttu-id="2bbe1-136">A operação de cópia ou movimentação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-136">The copy or move operation was successful.</span></span>
    
<span data-ttu-id="2bbe1-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="2bbe1-137">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="2bbe1-138">O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-138">The user canceled the operation, typically by clicking the **Cancel** button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="2bbe1-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="2bbe1-139">Remarks</span></span>

<span data-ttu-id="2bbe1-140">O método **IMAPISupport:: CopyMessages** é implementado para objetos de suporte do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-140">The **IMAPISupport::CopyMessages** method is implemented for message store provider support objects.</span></span> <span data-ttu-id="2bbe1-141">Os provedores de repositório de mensagens podem chamar **IMAPISupport:: CopyMessages** em sua implementação de [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) para copiar ou mover uma ou mais mensagens de uma pasta para outra.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-141">Message store providers can call **IMAPISupport::CopyMessages** in their implementation of [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) to copy or move one or more messages from one folder to another.</span></span> <span data-ttu-id="2bbe1-142">Como parte da chamada **IMAPISupport:: CopyMessages** , o provedor de repositório de mensagens pode especificar que o MAPI deve exibir um indicador de progresso.</span><span class="sxs-lookup"><span data-stu-id="2bbe1-142">As part of the **IMAPISupport::CopyMessages** call, the message store provider can specify that MAPI should display a progress indicator.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2bbe1-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2bbe1-143">See also</span></span>



[<span data-ttu-id="2bbe1-144">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="2bbe1-144">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
  
[<span data-ttu-id="2bbe1-145">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2bbe1-145">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

