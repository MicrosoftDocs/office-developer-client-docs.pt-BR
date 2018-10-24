---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583446"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="99851-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="99851-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="99851-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="99851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="99851-105">Realiza pós-processamento em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="99851-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="99851-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="99851-106">Parameters</span></span>

 <span data-ttu-id="99851-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="99851-107">_ulFlags_</span></span>
  
> <span data-ttu-id="99851-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="99851-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="99851-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="99851-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="99851-110">[in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="99851-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="99851-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="99851-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="99851-112">[in] Um ponteiro para o identificador de entrada da mensagem para processar.</span><span class="sxs-lookup"><span data-stu-id="99851-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="99851-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="99851-113">Return value</span></span>

<span data-ttu-id="99851-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="99851-114">S_OK</span></span> 
  
> <span data-ttu-id="99851-115">O pós-processamento foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="99851-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="99851-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="99851-116">Remarks</span></span>

<span data-ttu-id="99851-117">O método **IMAPISupport::CompleteMsg** é implementado para objetos de suporte do provedor de repositório de mensagem e é chamado somente por provedores de armazenamento de mensagem que estejam intimamente ligadas a provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="99851-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="99851-118">Provedores de armazenamento de ligação estreita chamarem **IMAPISupport::CompleteMsg** para instruir o spooler MAPI para postprocess uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="99851-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="99851-119">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="99851-119">Notes to callers</span></span>

<span data-ttu-id="99851-120">Chame **CompleteMsg** somente quando você está firmemente combinado com um provedor de transporte, você pode lidar com todos os destinatários da mensagem e houver uma das seguintes condições:</span><span class="sxs-lookup"><span data-stu-id="99851-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="99851-121">A mensagem foi pré-processado.</span><span class="sxs-lookup"><span data-stu-id="99851-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="99851-122">A mensagem requer pós-processamento pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="99851-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="99851-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="99851-123">See also</span></span>



[<span data-ttu-id="99851-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="99851-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

