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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767371"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="f0dba-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="f0dba-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="f0dba-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0dba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0dba-105">Recupera um fluxo a ser usado para salvar a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="f0dba-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="f0dba-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="f0dba-106">Parameters</span></span>

 <span data-ttu-id="f0dba-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="f0dba-107">_pulFlags_</span></span>
  
> <span data-ttu-id="f0dba-108">[out] Ponteiro para uma bitmask dos sinalizadores que controla como o texto da mensagem deve ser salvo.</span><span class="sxs-lookup"><span data-stu-id="f0dba-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="f0dba-109">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="f0dba-109">The following flag can be set:</span></span>
    
<span data-ttu-id="f0dba-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f0dba-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f0dba-111">O texto da mensagem é salvo no formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="f0dba-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="f0dba-112">Se o sinalizador MAPI_UNICODE não estiver definido, o texto é salvo no formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="f0dba-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="f0dba-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="f0dba-113">_pulFormat_</span></span>
  
> <span data-ttu-id="f0dba-114">[out] Ponteiro para uma bitmask dos sinalizadores que controla o formato do texto salvo.</span><span class="sxs-lookup"><span data-stu-id="f0dba-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="f0dba-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="f0dba-115">The following flags can be set:</span></span>
    
<span data-ttu-id="f0dba-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="f0dba-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="f0dba-117">O texto da mensagem deve ser salva como texto formatado em Rich Text Format (RTF).</span><span class="sxs-lookup"><span data-stu-id="f0dba-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="f0dba-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="f0dba-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="f0dba-119">O texto da mensagem deve ser salva como texto sem formatação.</span><span class="sxs-lookup"><span data-stu-id="f0dba-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="f0dba-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="f0dba-120">_ppstm_</span></span>
  
> <span data-ttu-id="f0dba-121">[out] Ponteiro para um ponteiro para o fluxo que conterá a mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="f0dba-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f0dba-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f0dba-122">Return value</span></span>

<span data-ttu-id="f0dba-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0dba-123">S_OK</span></span> 
  
> <span data-ttu-id="f0dba-124">O fluxo foi recuperado com êxito.</span><span class="sxs-lookup"><span data-stu-id="f0dba-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0dba-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="f0dba-125">Remarks</span></span>

<span data-ttu-id="f0dba-126">Objetos de formulário chame o método **IMAPIViewContext::GetSaveStream** para recuperar um fluxo de um objeto que implementa a interface **IStream** para oferecer suporte a manipulação do verbo Salvar como no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="f0dba-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="f0dba-127">O método [IMAPIForm::DoVerb](imapiform-doverb.md) , que é implementado no servidor de formulário e chamado pelo Visualizador do formulário para chamar um verbo, não deve retornar até que a mensagem é totalmente convertida em formato de texto apropriado e colocada no stream apropriado.</span><span class="sxs-lookup"><span data-stu-id="f0dba-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f0dba-128">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="f0dba-128">Notes to callers</span></span>

<span data-ttu-id="f0dba-129">Não grava no fluxo apontado pela _ppstm_ antes de chamar **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="f0dba-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="f0dba-130">Quando **GetSaveStream** retorna, não redefina a posição do ponteiro do seek.</span><span class="sxs-lookup"><span data-stu-id="f0dba-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="f0dba-131">Esse ponteiro deve permanecer no final do texto da mensagem salva.</span><span class="sxs-lookup"><span data-stu-id="f0dba-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0dba-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0dba-132">See also</span></span>



[<span data-ttu-id="f0dba-133">IMAPIViewContext: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f0dba-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

