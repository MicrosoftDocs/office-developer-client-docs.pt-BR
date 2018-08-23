---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9a5e4205a808c7a6e469d2e9cb0a1b3c17a92d21
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573541"
---
# <a name="imapiprogressgetflags"></a><span data-ttu-id="b394a-103">IMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b394a-103">IMAPIProgress::GetFlags</span></span>

  
  
<span data-ttu-id="b394a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b394a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b394a-105">Retorna sinaliza as configurações do objeto de andamento para o nível de operação no qual as informações sobre o andamento é calculado.</span><span class="sxs-lookup"><span data-stu-id="b394a-105">Returns flag settings from the progress object for the level of operation on which progress information is calculated.</span></span>
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="b394a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b394a-106">Parameters</span></span>

 <span data-ttu-id="b394a-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="b394a-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="b394a-108">[out] Uma bitmask dos sinalizadores que controla o nível de operação em andamento da qual as informações são calculadas.</span><span class="sxs-lookup"><span data-stu-id="b394a-108">[out] A bitmask of flags that controls the level of operation on which progress information is calculated.</span></span> <span data-ttu-id="b394a-109">O seguinte sinalizador pode ser retornado:</span><span class="sxs-lookup"><span data-stu-id="b394a-109">The following flag can be returned:</span></span>
    
<span data-ttu-id="b394a-110">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="b394a-110">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="b394a-111">Progresso está sendo calculado para o objeto de nível superior, o objeto que é chamado pelo cliente para iniciar a operação.</span><span class="sxs-lookup"><span data-stu-id="b394a-111">Progress is being calculated for the top-level object, the object that is called by the client to begin the operation.</span></span> <span data-ttu-id="b394a-112">Por exemplo, o objeto de nível superior em uma operação de cópia da pasta é a pasta que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="b394a-112">For example, the top-level object in a folder copy operation is the folder that is being copied.</span></span> <span data-ttu-id="b394a-113">Quando MAPI_TOP_LEVEL não estiver definida, o progresso é calculado para um objeto de nível inferior ou subobjeto.</span><span class="sxs-lookup"><span data-stu-id="b394a-113">When MAPI_TOP_LEVEL is not set, progress is calculated for a lower level object, or subobject.</span></span> <span data-ttu-id="b394a-114">Na operação de cópia de pasta, um objeto de nível inferior é uma das subpastas na pasta que está sendo copiada.</span><span class="sxs-lookup"><span data-stu-id="b394a-114">In the folder copy operation, a lower level object is one of the subfolders in the folder that is being copied.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b394a-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b394a-115">Return value</span></span>

<span data-ttu-id="b394a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="b394a-116">S_OK</span></span> 
  
> <span data-ttu-id="b394a-117">O valor flags foi retornado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b394a-117">The flags value was returned successfully.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b394a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="b394a-118">Remarks</span></span>

<span data-ttu-id="b394a-119">MAPI permite que os provedores de serviço diferenciar entre objetos de nível superior e subobjetos com o sinalizador MAPI_TOP_LEVEL para que todos os objetos envolvidos em uma operação podem usar a mesma implementação [IMAPIProgress](imapiprogressiunknown.md) para mostrar o progresso.</span><span class="sxs-lookup"><span data-stu-id="b394a-119">MAPI enables service providers to differentiate between top-level objects and subobjects with the MAPI_TOP_LEVEL flag so that all objects involved in an operation can use the same [IMAPIProgress](imapiprogressiunknown.md) implementation to show progress.</span></span> <span data-ttu-id="b394a-120">Isso faz com que a exibição de indicador prossiga normalmente em uma única direção positiva.</span><span class="sxs-lookup"><span data-stu-id="b394a-120">This causes the indicator display to proceed smoothly in a single positive direction.</span></span> <span data-ttu-id="b394a-121">Se o sinalizador MAPI_TOP_LEVEL está definido determina como provedores de serviços de definir os outros parâmetros em chamadas subsequentes ao objeto de andamento.</span><span class="sxs-lookup"><span data-stu-id="b394a-121">Whether the MAPI_TOP_LEVEL flag is set determines how service providers set the other parameters in subsequent calls to the progress object.</span></span> 
  
<span data-ttu-id="b394a-122">O valor retornado pela **GetFlags** é definido inicialmente pelo implementador e subsequentemente pelo provedor de serviços através de uma chamada ao método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) .</span><span class="sxs-lookup"><span data-stu-id="b394a-122">The value returned by **GetFlags** is set initially by the implementer and subsequently by the service provider through a call to the [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b394a-123">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="b394a-123">Notes to implementers</span></span>

<span data-ttu-id="b394a-124">Sempre inicializar o sinalizador para MAPI_TOP_LEVEL e depois contam com provedores de serviços para desmarcá-la quando apropriado.</span><span class="sxs-lookup"><span data-stu-id="b394a-124">Always initialize the flag to MAPI_TOP_LEVEL and then rely on service providers to clear it when appropriate.</span></span> <span data-ttu-id="b394a-125">Provedores de serviços podem desmarcar e redefinir o sinalizador chamando o método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="b394a-125">Service providers can clear and reset the flag by calling the **IMAPIProgress::SetLimits** method.</span></span> <span data-ttu-id="b394a-126">Para obter mais informações sobre como implementar **GetFlags** e outros métodos **IMAPIProgress** , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b394a-126">For more information about how to implement **GetFlags** and the other **IMAPIProgress** methods, see [Implementing a Progress Indicator](implementing-a-progress-indicator.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="b394a-127">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="b394a-127">Notes to callers</span></span>

<span data-ttu-id="b394a-128">Quando você exibe um indicador de progresso, faça uma chamada para **IMAPIProgress::GetFlags**para sua primeira chamada.</span><span class="sxs-lookup"><span data-stu-id="b394a-128">When you display a progress indicator, make your first call a call to **IMAPIProgress::GetFlags**.</span></span> <span data-ttu-id="b394a-129">O valor retornado deve ser MAPI_TOP_LEVEL, porque todas as implementações inicializar o conteúdo do parâmetro _lpulFlags_ para esse valor.</span><span class="sxs-lookup"><span data-stu-id="b394a-129">The returned value should be MAPI_TOP_LEVEL, because all implementations initialize the contents of the  _lpulFlags_ parameter to this value.</span></span> <span data-ttu-id="b394a-130">Para obter mais informações sobre a sequência de chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="b394a-130">For more information about the sequence of calls to a progress object, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b394a-131">Referência MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b394a-131">MFCMAPI reference</span></span>

<span data-ttu-id="b394a-132">Para exemplos de código MFCMAPI, consulte a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="b394a-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b394a-133">**Arquivo**</span><span class="sxs-lookup"><span data-stu-id="b394a-133">**File**</span></span>|<span data-ttu-id="b394a-134">**Function**</span><span class="sxs-lookup"><span data-stu-id="b394a-134">**Function**</span></span>|<span data-ttu-id="b394a-135">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b394a-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b394a-136">MAPIProgress.cpp</span><span class="sxs-lookup"><span data-stu-id="b394a-136">MAPIProgress.cpp</span></span>  <br/> |<span data-ttu-id="b394a-137">CMAPIProgress::GetFlags</span><span class="sxs-lookup"><span data-stu-id="b394a-137">CMAPIProgress::GetFlags</span></span>  <br/> |<span data-ttu-id="b394a-138">MFCMAPI usa o método **IMAPIProgress::GetFlags** para determinar quais sinalizadores estão definidos.</span><span class="sxs-lookup"><span data-stu-id="b394a-138">MFCMAPI uses the **IMAPIProgress::GetFlags** method to determine which flags are set.</span></span> <span data-ttu-id="b394a-139">Retorna MAPI_TOP_LEVEL, a menos que foram configuradas usando o método **IMAPIProgress::SetLimits** .</span><span class="sxs-lookup"><span data-stu-id="b394a-139">Returns MAPI_TOP_LEVEL unless flags have been set by using the **IMAPIProgress::SetLimits** method.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b394a-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="b394a-140">See also</span></span>



[<span data-ttu-id="b394a-141">IMAPIProgress::SetLimits</span><span class="sxs-lookup"><span data-stu-id="b394a-141">IMAPIProgress::SetLimits</span></span>](imapiprogress-setlimits.md)
  
[<span data-ttu-id="b394a-142">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b394a-142">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)


[<span data-ttu-id="b394a-143">MFCMAPI como um exemplo de código</span><span class="sxs-lookup"><span data-stu-id="b394a-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b394a-144">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="b394a-144">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)
  
[<span data-ttu-id="b394a-145">Implementar um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="b394a-145">Implementing a Progress Indicator</span></span>](implementing-a-progress-indicator.md)

