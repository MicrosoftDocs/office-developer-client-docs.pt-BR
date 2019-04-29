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
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411187"
---
# <a name="imapisupportcompletemsg"></a><span data-ttu-id="26ec7-103">IMAPISupport::CompleteMsg</span><span class="sxs-lookup"><span data-stu-id="26ec7-103">IMAPISupport::CompleteMsg</span></span>

  
  
<span data-ttu-id="26ec7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26ec7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26ec7-105">Executa o pré-processamento em uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="26ec7-105">Performs postprocessing on a message.</span></span> 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="26ec7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26ec7-106">Parameters</span></span>

 <span data-ttu-id="26ec7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="26ec7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="26ec7-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="26ec7-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="26ec7-109">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="26ec7-109">_cbEntryID_</span></span>
  
> <span data-ttu-id="26ec7-110">no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="26ec7-110">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="26ec7-111">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="26ec7-111">_lpEntryID_</span></span>
  
> <span data-ttu-id="26ec7-112">no Um ponteiro para o identificador de entrada da mensagem a ser processada.</span><span class="sxs-lookup"><span data-stu-id="26ec7-112">[in] A pointer to the entry identifier of the message to process.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26ec7-113">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="26ec7-113">Return value</span></span>

<span data-ttu-id="26ec7-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="26ec7-114">S_OK</span></span> 
  
> <span data-ttu-id="26ec7-115">O pré-processamento foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="26ec7-115">The postprocessing was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26ec7-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="26ec7-116">Remarks</span></span>

<span data-ttu-id="26ec7-117">O método **IMAPISupport:: CompleteMsg** é implementado para objetos de suporte do provedor de repositório de mensagens e é chamado apenas por provedores de repositório de mensagens firmemente acoplados a provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="26ec7-117">The **IMAPISupport::CompleteMsg** method is implemented for message store provider support objects and is called only by message store providers that are tightly coupled with transport providers.</span></span> <span data-ttu-id="26ec7-118">Provedores de repositório rigidamente acoplados chamam **IMAPISupport:: CompleteMsg** para instruir o spooler MAPI a postprocess uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="26ec7-118">Tightly coupled store providers call **IMAPISupport::CompleteMsg** to instruct the MAPI spooler to postprocess a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="26ec7-119">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="26ec7-119">Notes to callers</span></span>

<span data-ttu-id="26ec7-120">Chame **CompleteMsg** somente quando estiver rigidamente acoplado a um provedor de transporte, você pode lidar com todos os destinatários da mensagem e uma das seguintes condições existir:</span><span class="sxs-lookup"><span data-stu-id="26ec7-120">Call **CompleteMsg** only when you are tightly coupled with a transport provider, you can handle all of the message's recipients, and one of the following conditions exists:</span></span> 
  
- <span data-ttu-id="26ec7-121">A mensagem foi preprocessada.</span><span class="sxs-lookup"><span data-stu-id="26ec7-121">The message was preprocessed.</span></span>
    
- <span data-ttu-id="26ec7-122">A mensagem requer o pré-processamento pelo spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="26ec7-122">The message requires postprocessing by the MAPI spooler.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="26ec7-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="26ec7-123">See also</span></span>



[<span data-ttu-id="26ec7-124">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="26ec7-124">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

