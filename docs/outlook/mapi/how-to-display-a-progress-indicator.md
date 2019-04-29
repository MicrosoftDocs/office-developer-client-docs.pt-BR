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
# <a name="display-a-progress-indicator"></a>Exibir um indicador de progresso
 
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para exibir um indicador de progresso, chame [método imapiprogress:: GetFlags](imapiprogress-getflags.md) para recuperar a configuração de sinalizadores atual. 
  
Se o sinalizador MAPI_TOP_LEVEL estiver definido, conclua as seguintes etapas:
  
1. Definir uma variável igual ao número total de itens a serem processados na operação. Por exemplo, se você estiver copiando o conteúdo de uma pasta, esse valor será igual ao número das subpastas na pasta mais o número de mensagens. 
    
2. Definir uma variável igual a 1000 dividida pelo número de itens. 
    
3. Se você estiver mostrando o progresso de subobjetos, chame o método [método imapiprogress::](imapiprogress-setlimits.md) setlimits do objeto Progress e passe os seguintes valores para os três parâmetros: 
    
   - Defina o parâmetro _lpulMin_ como 0. 
    
   - Defina o parâmetro _lpulMax_ como 1000. 
    
   - Defina o parâmetro _lpulFlags_ como MAPI_TOP_LEVEL. 
    
4. Para cada objeto a ser processado, conclua as seguintes etapas:
    
   1. Chame **método imapiprogress::** setlimits e passe os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _lpulMin_ para o conjunto de variáveis na etapa 2 multiplicado pelo item atual menos 1. 
      
     - Defina o parâmetro _lpulMax_ para o conjunto de variáveis na etapa 2 multiplicado pelo objeto atual. 
      
     - Defina o parâmetro _lpulFlags_ como 0. 
      
   2. Execute qualquer processamento que deva ser feito nesse objeto. Se for um subobjeto e você quiser exibir o progresso em subobjetos, passe um ponteiro para o objeto Progress no parâmetro _lpProgress_ para o método. 
      
   3. Chame [método imapiprogress::P rogress](imapiprogress-progress.md) e passe os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _ulValue_ para o conjunto de variáveis na etapa 2 multiplicado pelo objeto atual. 
      
     - Defina o parâmetro _ulCount_ para o objeto atual. 
      
     - Defina o parâmetro _ulTotal_ para o conjunto de variáveis na etapa 1, o número total de objetos. 
    
Se o sinalizador MAPI_TOP_LEVEL não estiver definido, conclua as seguintes etapas:
  
1. Chame o método [método imapiprogress:: GetMin](imapiprogress-getmin.md) do objeto Progress para recuperar o valor mínimo para a exibição. 
    
2. Chame [método imapiprogress:: GetMax](imapiprogress-getmax.md) para recuperar o valor máximo para a exibição. 
    
3. Definir uma variável igual ao número total de objetos a serem processados. 
    
4. Definir uma variável igual ao resultado de subtrair o valor mínimo do valor máximo e, em seguida, dividindo pelo número total de objetos.
    
5. Para cada objeto a ser processado, conclua as seguintes etapas:
    
   1. Se seu provedor estiver mostrando o progresso de subobjetos, chame **método imapiprogress::** setlimits e passe os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _lpulMin_ para o valor mínimo mais o item atual menos 1 multiplicado pelo conjunto de variáveis na etapa 4. 
      
     - Defina o parâmetro _lpulMax_ para o valor mínimo mais a unidade atual multiplicada pelo conjunto de variáveis na etapa 4. 
      
     - Defina o parâmetro _lpulFlags_ como 0. 
      
   2. Execute qualquer processamento que deva ser feito nesse objeto. Se o objeto for um subobjeto e o seu provedor exibir o andamento dos subobjetos, passe um ponteiro para o objeto Progress no parâmetro _lpProgress_ para o método. 
      
   3. Chame [método imapiprogress::P rogress](imapiprogress-progress.md) e passe os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _ulValue_ como Variable Set na etapa 2 multiplicado pelo objeto atual. 
      
     - Defina o parâmetro _ulCount_ como 0. 
      
     - Defina o parâmetro _ulTotal_ como 0. 
    
O exemplo de código a seguir ilustra a lógica necessária para mostrar o progresso em todos os níveis de uma operação que copia o conteúdo de uma pasta que contém cinco subpastas. 
  
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

## <a name="see-also"></a>Confira também

- [Indicadores de progresso MAPI](mapi-progress-indicators.md)

