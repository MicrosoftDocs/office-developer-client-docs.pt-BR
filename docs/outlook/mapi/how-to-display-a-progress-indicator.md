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
ms.openlocfilehash: 62549cbeea0044ceee8aa2e704b8a9bc271b7e8e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564490"
---
# <a name="display-a-progress-indicator"></a><span data-ttu-id="8607f-103">Exibir um indicador de progresso</span><span class="sxs-lookup"><span data-stu-id="8607f-103">Display a progress indicator</span></span>
 
<span data-ttu-id="8607f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8607f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8607f-105">Para exibir um indicador de progresso, chame [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar os sinalizadores atuais definição.</span><span class="sxs-lookup"><span data-stu-id="8607f-105">To display a progress indicator, call [IMAPIProgress::GetFlags](imapiprogress-getflags.md) to retrieve the current flags setting.</span></span> 
  
<span data-ttu-id="8607f-106">Se o sinalizador MAPI_TOP_LEVEL estiver definido, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8607f-106">If the MAPI_TOP_LEVEL flag is set, complete the following steps:</span></span>
  
1. <span data-ttu-id="8607f-107">Defina uma variável igual ao número total de itens para processar na operação.</span><span class="sxs-lookup"><span data-stu-id="8607f-107">Set a variable equal to the total number of items to process in the operation.</span></span> <span data-ttu-id="8607f-108">Por exemplo, se você estiver copiando o conteúdo de uma pasta, esse valor será igual ao número de subpastas na pasta mais o número de mensagens.</span><span class="sxs-lookup"><span data-stu-id="8607f-108">For example, if you are copying the contents of a folder, this value will be equal to the number of the subfolders in the folder plus the number of messages.</span></span> 
    
2. <span data-ttu-id="8607f-109">Defina uma variável igual a 1000, divididos pelo número de itens.</span><span class="sxs-lookup"><span data-stu-id="8607f-109">Set a variable equal to 1000 divided by the number of items.</span></span> 
    
3. <span data-ttu-id="8607f-110">Se você está mostrando o andamento para subobjetos, chame o progresso método do objeto [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) e passar os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8607f-110">If you are showing progress for subobjects, call the progress object's [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) method and pass the following values for the three parameters:</span></span> 
    
   - <span data-ttu-id="8607f-111">Defina o parâmetro _lpulMin_ como 0.</span><span class="sxs-lookup"><span data-stu-id="8607f-111">Set the  _lpulMin_ parameter to 0.</span></span> 
    
   - <span data-ttu-id="8607f-112">Defina o parâmetro _lpulMax_ a 1000.</span><span class="sxs-lookup"><span data-stu-id="8607f-112">Set the  _lpulMax_ parameter to 1000.</span></span> 
    
   - <span data-ttu-id="8607f-113">Defina o parâmetro _lpulFlags_ para MAPI_TOP_LEVEL.</span><span class="sxs-lookup"><span data-stu-id="8607f-113">Set the  _lpulFlags_ parameter to MAPI_TOP_LEVEL.</span></span> 
    
4. <span data-ttu-id="8607f-114">Para cada objeto a serem processados, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8607f-114">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="8607f-115">Chame **IMAPIProgress::SetLimits** e passar os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8607f-115">Call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="8607f-116">Defina o parâmetro _lpulMin_ à variável definida na etapa 2 multiplicado pelo item atual menos 1.</span><span class="sxs-lookup"><span data-stu-id="8607f-116">Set the  _lpulMin_ parameter to the variable set in step 2 multiplied by the current item minus 1.</span></span> 
      
     - <span data-ttu-id="8607f-117">Defina o parâmetro _lpulMax_ à variável definida na etapa 2 multiplicado pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8607f-117">Set the  _lpulMax_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="8607f-118">Defina o parâmetro _lpulFlags_ como 0.</span><span class="sxs-lookup"><span data-stu-id="8607f-118">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="8607f-119">Execute qualquer processamento deve ser feito neste objeto.</span><span class="sxs-lookup"><span data-stu-id="8607f-119">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="8607f-120">Se este for um Subobjeto e você deseja exibir o progresso em subobjetos, passe um ponteiro para o objeto de andamento no parâmetro _lpProgress_ para o método.</span><span class="sxs-lookup"><span data-stu-id="8607f-120">If this is a subobject and you want to display progress on subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="8607f-121">Chame [IMAPIProgress::Progress](imapiprogress-progress.md) e passar os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8607f-121">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="8607f-122">Defina o parâmetro _ulValue_ à variável definida na etapa 2 multiplicado pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8607f-122">Set the  _ulValue_ parameter to the variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="8607f-123">Defina o parâmetro _ulCount_ ao objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8607f-123">Set the  _ulCount_ parameter to the current object.</span></span> 
      
     - <span data-ttu-id="8607f-124">Defina o parâmetro _ulTotal_ para a variável definida na etapa 1, o número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="8607f-124">Set the  _ulTotal_ parameter to the variable set in step 1, the total number of objects.</span></span> 
    
<span data-ttu-id="8607f-125">Se o sinalizador MAPI_TOP_LEVEL não estiver definido, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8607f-125">If the MAPI_TOP_LEVEL flag is not set, complete the following steps:</span></span>
  
1. <span data-ttu-id="8607f-126">Chame o progresso método do objeto [IMAPIProgress::GetMin](imapiprogress-getmin.md) para recuperar o valor mínimo para a exibição.</span><span class="sxs-lookup"><span data-stu-id="8607f-126">Call the progress object's [IMAPIProgress::GetMin](imapiprogress-getmin.md) method to retrieve the minimum value for the display.</span></span> 
    
2. <span data-ttu-id="8607f-127">Chame [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar o valor máximo da tela.</span><span class="sxs-lookup"><span data-stu-id="8607f-127">Call [IMAPIProgress::GetMax](imapiprogress-getmax.md) to retrieve the maximum value for the display.</span></span> 
    
3. <span data-ttu-id="8607f-128">Defina uma variável igual ao número total de objetos a serem processados.</span><span class="sxs-lookup"><span data-stu-id="8607f-128">Set a variable equal to the total number of objects to be processed.</span></span> 
    
4. <span data-ttu-id="8607f-129">Defina uma variável igual ao resultado da subtraindo o valor mínimo do valor máximo e, em seguida, dividindo pelo número total de objetos.</span><span class="sxs-lookup"><span data-stu-id="8607f-129">Set a variable equal to the result of subtracting the minimum value from the maximum value and then dividing by the total number of objects.</span></span>
    
5. <span data-ttu-id="8607f-130">Para cada objeto a serem processados, conclua as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="8607f-130">For each object to be processed, complete the following steps:</span></span>
    
   1. <span data-ttu-id="8607f-131">Se seu provedor estiver mostrando o andamento para subobjetos, chame **IMAPIProgress::SetLimits** e passar os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8607f-131">If your provider is showing progress for subobjects, call **IMAPIProgress::SetLimits** and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="8607f-132">Defina o parâmetro _lpulMin_ para o valor mínimo além do item atual menos 1 multiplicado pela variável definida na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="8607f-132">Set the  _lpulMin_ parameter to the minimum value plus the current item minus 1 multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="8607f-133">Defina o parâmetro _lpulMax_ como o valor mínimo mais a unidade atual multiplicado pela variável definida na etapa 4.</span><span class="sxs-lookup"><span data-stu-id="8607f-133">Set the  _lpulMax_ parameter to the minimum value plus the current unit multiplied by the variable set in step 4.</span></span> 
      
     - <span data-ttu-id="8607f-134">Defina o parâmetro _lpulFlags_ como 0.</span><span class="sxs-lookup"><span data-stu-id="8607f-134">Set the  _lpulFlags_ parameter to 0.</span></span> 
      
   2. <span data-ttu-id="8607f-135">Execute qualquer processamento deve ser feito neste objeto.</span><span class="sxs-lookup"><span data-stu-id="8607f-135">Perform whatever processing should be done on this object.</span></span> <span data-ttu-id="8607f-136">Se o objeto é um Subobjeto e seu provedor exibe o andamento para subobjetos, passe um ponteiro para o objeto de andamento no parâmetro _lpProgress_ para o método.</span><span class="sxs-lookup"><span data-stu-id="8607f-136">If the object is a subobject, and your provider displays progress for subobjects, pass a pointer to the progress object in the  _lpProgress_ parameter to the method.</span></span> 
      
   3. <span data-ttu-id="8607f-137">Chame [IMAPIProgress::Progress](imapiprogress-progress.md) e passar os seguintes valores para os três parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8607f-137">Call [IMAPIProgress::Progress](imapiprogress-progress.md) and pass the following values for the three parameters:</span></span> 
      
     - <span data-ttu-id="8607f-138">Defina o parâmetro _ulValue_ a variável definida na etapa 2 multiplicado pelo objeto atual.</span><span class="sxs-lookup"><span data-stu-id="8607f-138">Set the  _ulValue_ parameter to variable set in step 2 multiplied by the current object.</span></span> 
      
     - <span data-ttu-id="8607f-139">Defina o parâmetro _ulCount_ como 0.</span><span class="sxs-lookup"><span data-stu-id="8607f-139">Set the  _ulCount_ parameter to 0.</span></span> 
      
     - <span data-ttu-id="8607f-140">Defina o parâmetro _ulTotal_ como 0.</span><span class="sxs-lookup"><span data-stu-id="8607f-140">Set the  _ulTotal_ parameter to 0.</span></span> 
    
<span data-ttu-id="8607f-141">O exemplo de código a seguir ilustra a lógica necessária para mostrar o progresso em todos os níveis de uma operação que copia o conteúdo de uma pasta que contém cinco subpastas.</span><span class="sxs-lookup"><span data-stu-id="8607f-141">The following code example illustrates the logic required to show progress at all levels of an operation that copies the contents of a folder that contains five subfolders.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="8607f-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="8607f-142">See also</span></span>

- [<span data-ttu-id="8607f-143">Indicadores de progresso MAPI</span><span class="sxs-lookup"><span data-stu-id="8607f-143">MAPI Progress Indicators</span></span>](mapi-progress-indicators.md)

