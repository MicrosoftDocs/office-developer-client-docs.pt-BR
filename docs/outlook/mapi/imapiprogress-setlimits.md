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
  
> no Um ponteiro para uma variável que contém o limite inferior dos itens na operação.
    
 _lpulMax_
  
> no Um ponteiro para uma variável que contém o limite superior de itens na operação.
    
 _lpulFlags_
  
> no Uma bitmask de sinalizadores que controla o nível de operação no qual as informações de progresso são calculadas. O seguinte sinalizador pode ser definido:
    
MAPI_TOP_LEVEL 
  
> Usa os valores dos parâmetros _ulCount_ e _UlTotal_ do método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indicam o item processado atualmente e o total de itens, respectivamente, para incrementar o progresso na operação. Quando esse sinalizador é definido, os valores dos limites global inferior e superior precisam ser definidos. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de serviços chamam o método **método imapiprogress::** setlimits para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores mínimos e globais locais e máximos. O valor da configuração do sinalizador afeta se o objeto Progress entende os valores mínimo e máximo para serem local ou global. Quando o sinalizador MAPI_TOP_LEVEL é definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação. Os objetos Progress inicializam o valor mínimo global como 1 e o valor global máximo como 1000. 
  
Quando MAPI_TOP_LEVEL não estiver definido, os valores mínimo e máximo serão considerados locais e os provedores os usarão internamente para exibir o progresso dos subobjetos de nível inferior. Os objetos Progress salvam os valores mínimo e máximo locais apenas para que eles possam ser retornados aos provedores quando os métodos [método imapiprogress:: GetMin](imapiprogress-getmin.md) e [método imapiprogress:: GetMax](imapiprogress-getmax.md) são chamados. 
  
Para obter mais informações sobre como implementar **** setlimits e os outros métodos do [método imapiprogress](imapiprogressiunknown.md) , consulte [implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: setLimits  <br/> |MFCMAPI usa o método **método imapiprogress::** setlimits para definir os limites máximo e mínimo e os sinalizadores para o objeto Progress.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

