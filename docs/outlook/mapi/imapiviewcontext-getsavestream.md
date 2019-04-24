---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351118"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="2ed3a-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="2ed3a-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="2ed3a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ed3a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ed3a-105">Recupera um fluxo a ser usado para salvar a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="2ed3a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ed3a-106">Parameters</span></span>

 <span data-ttu-id="2ed3a-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="2ed3a-107">_pulFlags_</span></span>
  
> <span data-ttu-id="2ed3a-108">bota Ponteiro para uma bitmask de sinalizadores que controla como o texto da mensagem deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="2ed3a-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="2ed3a-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2ed3a-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2ed3a-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2ed3a-111">O texto da mensagem é salvo no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="2ed3a-112">Se o sinalizador MAPI_UNICODE não estiver definido, o texto será salvo no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="2ed3a-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="2ed3a-113">_pulFormat_</span></span>
  
> <span data-ttu-id="2ed3a-114">bota Ponteiro para uma bitmask de sinalizadores que controla o formato do texto salvo.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="2ed3a-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="2ed3a-115">The following flags can be set:</span></span>
    
<span data-ttu-id="2ed3a-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="2ed3a-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="2ed3a-117">O texto da mensagem deve ser salvo como texto formatado no formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="2ed3a-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="2ed3a-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="2ed3a-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="2ed3a-119">O texto da mensagem deve ser salvo como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="2ed3a-120">_ppStm_</span><span class="sxs-lookup"><span data-stu-id="2ed3a-120">_ppstm_</span></span>
  
> <span data-ttu-id="2ed3a-121">bota Ponteiro para um ponteiro para o Stream que conterá a mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ed3a-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2ed3a-122">Return value</span></span>

<span data-ttu-id="2ed3a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ed3a-123">S_OK</span></span> 
  
> <span data-ttu-id="2ed3a-124">O fluxo foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2ed3a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ed3a-125">Remarks</span></span>

<span data-ttu-id="2ed3a-126">Os objetos Form chamam o método **IMAPIViewContext:: GetSaveStream** para recuperar um objeto Stream que implementa a interface **IStream** para suportar o tratamento do verbo salvar como no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="2ed3a-127">O método [IMAPIForm::D overb](imapiform-doverb.md) , que é implementado no servidor de formulário e chamado pelo Visualizador de formulários para invocar um verbo, não deve ser retornado até que a mensagem seja totalmente convertida no formato de texto apropriado e colocado no fluxo apropriado.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2ed3a-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2ed3a-128">Notes to callers</span></span>

<span data-ttu-id="2ed3a-129">Não grave no fluxo apontado pelo _ppStm_ antes de chamar **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="2ed3a-130">Quando **GetSaveStream** retorna, não redefine a posição do ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="2ed3a-131">Esse ponteiro deve permanecer no final do texto da mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="2ed3a-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ed3a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ed3a-132">See also</span></span>



[<span data-ttu-id="2ed3a-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ed3a-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

