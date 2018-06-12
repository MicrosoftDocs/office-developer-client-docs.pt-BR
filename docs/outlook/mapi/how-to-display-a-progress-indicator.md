---
title: Exibir um indicador de progresso
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 20f5ad5a-b700-4fb5-9658-f71da5a06a12
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3c4c553a000dab233eb208c1222cc427c97b1e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766720"
---
# <a name="display-a-progress-indicator"></a>Exibir um indicador de progresso
 
**Aplica-se a**: Outlook 
  
Para exibir um indicador de progresso, chame [IMAPIProgress::GetFlags](imapiprogress-getflags.md) para recuperar os sinalizadores atuais definição. 
  
Se o sinalizador MAPI_TOP_LEVEL estiver definido, conclua as seguintes etapas:
  
1. Defina uma variável igual ao número total de itens para processar na operação. Por exemplo, se você estiver copiando o conteúdo de uma pasta, esse valor será igual ao número de subpastas na pasta mais o número de mensagens. 
    
2. Defina uma variável igual a 1000, divididos pelo número de itens. 
    
3. Se você está mostrando o andamento para subobjetos, chame o progresso método do objeto [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) e passar os seguintes valores para os três parâmetros: 
    
   - Defina o parâmetro _lpulMin_ como 0. 
    
   - Defina o parâmetro _lpulMax_ a 1000. 
    
   - Defina o parâmetro _lpulFlags_ para MAPI_TOP_LEVEL. 
    
4. Para cada objeto a serem processados, conclua as seguintes etapas:
    
   1. Chame **IMAPIProgress::SetLimits** e passar os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _lpulMin_ à variável definida na etapa 2 multiplicado pelo item atual menos 1. 
      
     - Defina o parâmetro _lpulMax_ à variável definida na etapa 2 multiplicado pelo objeto atual. 
      
     - Defina o parâmetro _lpulFlags_ como 0. 
      
   2. Execute qualquer processamento deve ser feito neste objeto. Se este for um Subobjeto e você deseja exibir o progresso em subobjetos, passe um ponteiro para o objeto de andamento no parâmetro _lpProgress_ para o método. 
      
   3. Chame [IMAPIProgress::Progress](imapiprogress-progress.md) e passar os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _ulValue_ à variável definida na etapa 2 multiplicado pelo objeto atual. 
      
     - Defina o parâmetro _ulCount_ ao objeto atual. 
      
     - Defina o parâmetro _ulTotal_ para a variável definida na etapa 1, o número total de objetos. 
    
Se o sinalizador MAPI_TOP_LEVEL não estiver definido, conclua as seguintes etapas:
  
1. Chame o progresso método do objeto [IMAPIProgress::GetMin](imapiprogress-getmin.md) para recuperar o valor mínimo para a exibição. 
    
2. Chame [IMAPIProgress::GetMax](imapiprogress-getmax.md) para recuperar o valor máximo da tela. 
    
3. Defina uma variável igual ao número total de objetos a serem processados. 
    
4. Defina uma variável igual ao resultado da subtraindo o valor mínimo do valor máximo e, em seguida, dividindo pelo número total de objetos.
    
5. Para cada objeto a serem processados, conclua as seguintes etapas:
    
   1. Se seu provedor estiver mostrando o andamento para subobjetos, chame **IMAPIProgress::SetLimits** e passar os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _lpulMin_ para o valor mínimo além do item atual menos 1 multiplicado pela variável definida na etapa 4. 
      
     - Defina o parâmetro _lpulMax_ como o valor mínimo mais a unidade atual multiplicado pela variável definida na etapa 4. 
      
     - Defina o parâmetro _lpulFlags_ como 0. 
      
   2. Execute qualquer processamento deve ser feito neste objeto. Se o objeto é um Subobjeto e seu provedor exibe o andamento para subobjetos, passe um ponteiro para o objeto de andamento no parâmetro _lpProgress_ para o método. 
      
   3. Chame [IMAPIProgress::Progress](imapiprogress-progress.md) e passar os seguintes valores para os três parâmetros: 
      
     - Defina o parâmetro _ulValue_ a variável definida na etapa 2 multiplicado pelo objeto atual. 
      
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

