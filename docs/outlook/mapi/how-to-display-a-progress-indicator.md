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
  
Para exibir um indicador de progresso, chame [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar a configuração de sinalizadores atual. 
  
Se o MAPI_TOP_LEVEL sinalizador estiver definido, conclua as seguintes etapas:
  
1. Definir uma variável igual ao número total de itens a processar na operação. Por exemplo, se você estiver copiando o conteúdo de uma pasta, esse valor será igual ao número de subpastas na pasta mais o número de mensagens. 
    
2. Definir uma variável igual a 1000 dividido pelo número de itens. 
    
3. Se você estiver mostrando o progresso de subobjetos, chame o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) do objeto de progresso e passe os seguintes valores para os três parâmetros: 
    
   - De definir  _o parâmetro lpulMin_ como 0. 
    
   - De definir  _o parâmetro lpulMax_ como 1000. 
    
   - Defina  _o parâmetro lpulFlags_ como MAPI_TOP_LEVEL. 
    
4. Para cada objeto a ser processado, conclua as seguintes etapas:
    
   1. Chame **IMAPIProgress::SetLimits** e passe os seguintes valores para os três parâmetros: 
      
     - Definir o  _parâmetro lpulMin_ como a variável definida na etapa 2 multiplicada pelo item atual menos 1. 
      
     - De definir  _o parâmetro lpulMax_ como a variável definida na etapa 2 multiplicada pelo objeto atual. 
      
     - Defina  _o parâmetro lpulFlags_ como 0. 
      
   2. Execute qualquer processamento que deva ser feito nesse objeto. Se for um subobjeto e você quiser exibir o progresso em subobjetos, passe um ponteiro para o objeto de progresso no parâmetro  _lpProgress_ para o método. 
      
   3. Chame [IMAPIProgress::P e](imapiprogress-progress.md) passe os seguintes valores para os três parâmetros: 
      
     - De definir  _o parâmetro ulValue_ como a variável definida na etapa 2 multiplicada pelo objeto atual. 
      
     - De definir  _o parâmetro ulCount_ para o objeto atual. 
      
     - Definir o  _parâmetro ulTotal_ como a variável definida na etapa 1, o número total de objetos. 
    
Se o MAPI_TOP_LEVEL sinalizador não estiver definido, conclua as seguintes etapas:
  
1. Chame o método [IMAPIProgress::GetMin](imapiprogress-getmin.md) do objeto de progresso para recuperar o valor mínimo para a exibição. 
    
2. Chame [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar o valor máximo da exibição. 
    
3. Definir uma variável igual ao número total de objetos a serem processados. 
    
4. Definir uma variável igual ao resultado da subtração do valor mínimo do valor máximo e, em seguida, dividir pelo número total de objetos.
    
5. Para cada objeto a ser processado, conclua as seguintes etapas:
    
   1. Se o provedor estiver mostrando o progresso de subobjetos, chame **IMAPIProgress::SetLimits** e passe os seguintes valores para os três parâmetros: 
      
     - De definir  _o parâmetro lpulMin_ como o valor mínimo mais o item atual menos 1 multiplicado pela variável definida na etapa 4. 
      
     - De definir  _o parâmetro lpulMax_ como o valor mínimo mais a unidade atual multiplicada pela variável definida na etapa 4. 
      
     - Defina  _o parâmetro lpulFlags_ como 0. 
      
   2. Execute qualquer processamento que deva ser feito nesse objeto. Se o objeto for um subobjeto e seu provedor exibir o progresso de subobjetos, passe um ponteiro para o objeto de progresso no parâmetro  _lpProgress_ para o método. 
      
   3. Chame [IMAPIProgress::P e](imapiprogress-progress.md) passe os seguintes valores para os três parâmetros: 
      
     - De definir  _o parâmetro ulValue_ como variável definida na etapa 2 multiplicada pelo objeto atual. 
      
     - De definir  _o parâmetro ulCount_ como 0. 
      
     - De definir  _o parâmetro ulTotal_ como 0. 
    
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

