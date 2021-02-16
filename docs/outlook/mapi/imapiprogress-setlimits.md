---
title: IMAPIProgressSetLimits
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.SetLimits
api_type:
- COM
ms.assetid: 63c9e316-ee53-4065-8154-449639643ff7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0810ed7ce20bba95c4286e6e042065c0c2d1a802
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421463"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define os limites inferior e superior para o número de itens na operação e os sinalizadores que controlam como as informações de progresso são calculadas para a operação.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulMin_
  
> [in] Um ponteiro para uma variável que contém o limite inferior de itens na operação.
    
 _lpulMax_
  
> [in] Um ponteiro para uma variável que contém o limite superior de itens na operação.
    
 _lpulFlags_
  
> [in] Uma bitmask de sinalizadores que controla o nível de operação no qual as informações de progresso são calculadas. O sinalizador a seguir pode ser definido:
    
MAPI_TOP_LEVEL 
  
> Usa os valores nos parâmetros _ulCount_ e _ulTotal_ do método [IMAPIProgress::P ess,](imapiprogress-progress.md) que indicam o item processado no momento e o total de itens, respectivamente, para incrementar o progresso da operação. Quando esse sinalizador é definido, os valores dos limites superiores e inferiores globais devem ser definidos. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de serviços chamam o método **IMAPIProgress::SetLimits** para definir ou limpar o sinalizador MAPI_TOP_LEVEL e definir valores mínimo e máximo locais e globais. O valor da configuração do sinalizador afeta se o objeto de progresso entende os valores mínimo e máximo para serem locais ou globais. Quando o MAPI_TOP_LEVEL sinalizador é definido, esses valores são considerados globais e usados para calcular o progresso de toda a operação. Os objetos de progresso inicializam o valor mínimo global como 1 e o valor máximo global como 1000. 
  
Quando MAPI_TOP_LEVEL não está definido, os valores mínimo e máximo são considerados locais, e os provedores os usam internamente para exibir o progresso de subobjetos de nível inferior. Os objetos de progresso salvam os valores mínimo e máximo local apenas para que possam ser retornados aos provedores quando os métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax](imapiprogress-getmax.md) são chamados. 
  
Para obter mais informações sobre como implementar **SetLimits** e outros [métodos IMAPIProgress,](imapiprogressiunknown.md) consulte [Implementando um indicador de progresso.](implementing-a-progress-indicator.md)
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI usa o método **IMAPIProgress::SetLimits** para definir os limites máximo e mínimo e sinalizadores para o objeto de progresso.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

