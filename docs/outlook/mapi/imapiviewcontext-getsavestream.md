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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408422"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="a5621-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="a5621-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="a5621-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a5621-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a5621-105">Recupera um fluxo a ser usado para salvar a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="a5621-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="a5621-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a5621-106">Parameters</span></span>

 <span data-ttu-id="a5621-107">_lagFlags_</span><span class="sxs-lookup"><span data-stu-id="a5621-107">_pulFlags_</span></span>
  
> <span data-ttu-id="a5621-108">[out] Ponteiro para uma máscara de bits de sinalizadores que controla como o texto da mensagem deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="a5621-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="a5621-109">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="a5621-109">The following flag can be set:</span></span>
    
<span data-ttu-id="a5621-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a5621-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a5621-111">O texto da mensagem é salvo no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="a5621-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="a5621-112">Se o MAPI_UNICODE não estiver definido, o texto será salvo no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="a5621-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="a5621-113">_milaFormat_</span><span class="sxs-lookup"><span data-stu-id="a5621-113">_pulFormat_</span></span>
  
> <span data-ttu-id="a5621-114">[out] Ponteiro para uma máscara de bits de sinalizadores que controla o formato do texto salvo.</span><span class="sxs-lookup"><span data-stu-id="a5621-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="a5621-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="a5621-115">The following flags can be set:</span></span>
    
<span data-ttu-id="a5621-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="a5621-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="a5621-117">O texto da mensagem deve ser salvo como texto formatado no formato Rich Text (RTF).</span><span class="sxs-lookup"><span data-stu-id="a5621-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="a5621-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="a5621-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="a5621-119">O texto da mensagem deve ser salvo como texto sem texto simples.</span><span class="sxs-lookup"><span data-stu-id="a5621-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="a5621-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="a5621-120">_ppstm_</span></span>
  
> <span data-ttu-id="a5621-121">[out] Ponteiro para um ponteiro para o fluxo que conterá a mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="a5621-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a5621-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a5621-122">Return value</span></span>

<span data-ttu-id="a5621-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a5621-123">S_OK</span></span> 
  
> <span data-ttu-id="a5621-124">O fluxo foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="a5621-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a5621-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5621-125">Remarks</span></span>

<span data-ttu-id="a5621-126">Objetos de formulário chamam o método **IMAPIViewContext::GetSaveStream** para recuperar um fluxo de um objeto que implementa a interface **IStream** para suportar a manipulação do verbo Salvar como no visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="a5621-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="a5621-127">O método [IMAPIForm::D oVerb,](imapiform-doverb.md) que é implementado no servidor de formulário e chamado pelo visualizador de formulário para invocar um verbo, não deve retornar até que a mensagem seja totalmente convertida no formato de texto apropriado e colocada no fluxo apropriado.</span><span class="sxs-lookup"><span data-stu-id="a5621-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a5621-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="a5621-128">Notes to callers</span></span>

<span data-ttu-id="a5621-129">Não escreva no fluxo apontado pelo  _ppstm_ antes de chamar **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="a5621-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="a5621-130">Quando **GetSaveStream** retornar, não redefinir a posição do ponteiro de busca.</span><span class="sxs-lookup"><span data-stu-id="a5621-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="a5621-131">Este ponteiro deve permanecer no final do texto da mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="a5621-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a5621-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a5621-132">See also</span></span>



[<span data-ttu-id="a5621-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a5621-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

