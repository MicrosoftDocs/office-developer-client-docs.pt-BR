---
title: Exibir um indicador de progresso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7b0ce0ab75ffdce045ccde5bf6ea8a7da046f463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408023"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="60cf1-103">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="60cf1-103">Display a progress indicator</span></span>
 
<span data-ttu-id="60cf1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60cf1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60cf1-105">Para exibir um indicador de progresso, chame [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar a configuração de sinalizadores atual.</span><span class="sxs-lookup"><span data-stu-id="60cf1-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="60cf1-106">Se o MAPI_TOP_LEVEL sinalizador estiver definido, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="60cf1-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="60cf1-107">Definir uma variável igual ao número total de itens a processar na operação.</span><span class="sxs-lookup"><span data-stu-id="60cf1-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="60cf1-108">Por exemplo, se você estiver copiando o conteúdo de uma pasta, esse valor será igual ao número de subpastas na pasta mais o número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="60cf1-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="60cf1-109">Definir uma variável igual a 1000 dividido pelo número de itens.</span><span class="sxs-lookup"><span data-stu-id="60cf1-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="60cf1-110">Se você estiver mostrando o progresso de subobjetos, chame o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) do objeto de progresso e passe os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="60cf1-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="60cf1-111">De definir  _o parâmetro lpulMin_ como 0.</span><span class="sxs-lookup"><span data-stu-id="60cf1-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="60cf1-112">De definir  _o parâmetro lpulMax_ como 1000.</span><span class="sxs-lookup"><span data-stu-id="60cf1-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="60cf1-113">Defina  _o parâmetro lpulFlags_ como MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="60cf1-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="60cf1-114">Para cada objeto a ser processado, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="60cf1-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="60cf1-115">Chame **IMAPIProgress::SetLimits** e passe os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="60cf1-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="60cf1-116">Definir o  _parâmetro lpulMin_ como a variável definida na etapa 2 multiplicada pelo item atual menos 1.</span><span class="sxs-lookup"><span data-stu-id="60cf1-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="60cf1-117">De definir  _o parâmetro lpulMax_ como a variável definida na etapa 2 multiplicada pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="60cf1-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="60cf1-118">Defina  _o parâmetro lpulFlags_ como 0.</span><span class="sxs-lookup"><span data-stu-id="60cf1-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="60cf1-119">Execute qualquer processamento que deva ser feito nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="60cf1-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="60cf1-120">Se for um subobjeto e você quiser exibir o progresso em subobjetos, passe um ponteiro para o objeto de progresso no parâmetro  _lpProgress_ para o método.</span><span class="sxs-lookup"><span data-stu-id="60cf1-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="60cf1-121">Chame [IMAPIProgress::P e](imapiprogress-progress.md) passe os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="60cf1-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="60cf1-122">De definir  _o parâmetro ulValue_ como a variável definida na etapa 2 multiplicada pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="60cf1-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="60cf1-123">De definir  _o parâmetro ulCount_ para o objeto atual.</span><span class="sxs-lookup"><span data-stu-id="60cf1-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="60cf1-124">Definir o  _parâmetro ulTotal_ como a variável definida na etapa 1, o número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="60cf1-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="60cf1-125">Se o MAPI_TOP_LEVEL sinalizador não estiver definido, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="60cf1-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="60cf1-126">Chame o método [IMAPIProgress::GetMin](imapiprogress-getmin.md) do objeto de progresso para recuperar o valor mínimo para a exibição.</span><span class="sxs-lookup"><span data-stu-id="60cf1-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="60cf1-127">Chame [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar o valor máximo da exibição.</span><span class="sxs-lookup"><span data-stu-id="60cf1-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="60cf1-128">Definir uma variável igual ao número total de objetos a serem processados.</span><span class="sxs-lookup"><span data-stu-id="60cf1-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="60cf1-129">Definir uma variável igual ao resultado da subtração do valor mínimo do valor máximo e, em seguida, dividir pelo número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="60cf1-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="60cf1-130">Para cada objeto a ser processado, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="60cf1-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="60cf1-131">Se o provedor estiver mostrando o progresso de subobjetos, chame **IMAPIProgress::SetLimits** e passe os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="60cf1-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="60cf1-132">De definir  _o parâmetro lpulMin_ como o valor mínimo mais o item atual menos 1 multiplicado pela variável definida na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="60cf1-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="60cf1-133">De definir  _o parâmetro lpulMax_ como o valor mínimo mais a unidade atual multiplicada pela variável definida na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="60cf1-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="60cf1-134">Defina  _o parâmetro lpulFlags_ como 0.</span><span class="sxs-lookup"><span data-stu-id="60cf1-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="60cf1-135">Execute qualquer processamento que deva ser feito nesse objeto.</span><span class="sxs-lookup"><span data-stu-id="60cf1-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="60cf1-136">Se o objeto for um subobjeto e seu provedor exibir o progresso de subobjetos, passe um ponteiro para o objeto de progresso no parâmetro  _lpProgress_ para o método.</span><span class="sxs-lookup"><span data-stu-id="60cf1-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="60cf1-137">Chame [IMAPIProgress::P e](imapiprogress-progress.md) passe os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="60cf1-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="60cf1-138">De definir  _o parâmetro ulValue_ como variável definida na etapa 2 multiplicada pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="60cf1-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="60cf1-139">De definir  _o parâmetro ulCount_ como 0.</span><span class="sxs-lookup"><span data-stu-id="60cf1-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="60cf1-140">De definir  _o parâmetro ulTotal_ como 0.</span><span class="sxs-lookup"><span data-stu-id="60cf1-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="60cf1-141">O exemplo de código a seguir ilustra a lógica necessária para mostrar o progresso em todos os níveis de uma operação que copia o conteúdo de uma pasta que contém cinco subpastas.</span><span class="sxs-lookup"><span data-stu-id="60cf1-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
```cpp
lpProgress->GetFlags (lpulFlags);
ulFlags = *lpulFlags;
/* The folder in charge of the display. It contains 5 subfolders. */
if (ulFlags & MAPI_TOP_LEVEL)
{
    ulItems = 5                         // 5 subfolders in this folder
    ulScale = (ulMax / ulItems)         // 200 because ulMax = 1000
    lpProgress->SetLimits(0, ulMax, MAPI_TOP_LEVEL)
    for (i = 1; i <= ulItems; i++)      // for each subfolder to copy
    {
        lpProgress->SetLimits( (i - 1) * ulScale, i * ulScale, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        lpProgress->Progress( i * ulScale, i, ulItems)
    }
}
else
/* One of the subfolders to be copied. It contains 3 messages. */
{
    lpProgress->GetMin(&ulMin);
    lpProgress->GetMax(&ulMax);
    ulItems = 3;
    ulDelta = (ulMax - ulMin) / ulItems;
    for (i = 1; i <= ulItems; i++)
    {
        lpProgress->SetLimits(ulMin + (i - 1) * ulDelta,
                              ulMin + i * ulDelta, 0)
        CopyOneFolder(lpFolder(i), lpProgress)
        /* Pass 0 for ulCount and ulTotal because this is not the */
        /* top-level display, and that information is unavailable  */
        lpProgress->Progress( i * ulDelta, 0, 0)
    }
}
 
```

## <a name="see-also"></a><span data-ttu-id="60cf1-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="60cf1-142">See also</span></span>

- [<span data-ttu-id="60cf1-143">Indicadores de progresso MAPI</span><span class="sxs-lookup"><span data-stu-id="60cf1-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

