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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 14abfaadcdb1710a7cb8275c8f82d502aea8300e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767133"
---
# <a name="imapiprogresssetlimits"></a>IMAPIProgress::SetLimits

  
  
**Aplica-se a**: Outlook 
  
Define os limites inferiores e superiores para o número de itens da operação e os sinalizadores que controlam como as informações sobre o andamento é calculada para a operação.
  
```cpp
HRESULT SetLimits(
  LPULONG lpulMin,
  LPULONG lpulMax,
  LPULONG lpulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpulMin_
  
> [in] Um ponteiro para uma variável que contenha o limite inferior dos itens na operação.
    
 _lpulMax_
  
> [in] Um ponteiro para uma variável que contenha o limite superior dos itens na operação.
    
 _lpulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o nível de operação em andamento da qual as informações são calculadas. O seguinte sinalizador pode ser definido:
    
MAPI_TOP_LEVEL 
  
> Usa os valores do método [IMAPIProgress::Progress](imapiprogress-progress.md) _ulCount_ _ulTotal_ parâmetros e, que indica o item atualmente processado e o total de itens, respectivamente, para o progresso de incremento sobre a operação. Quando esse sinalizador estiver definido, os valores dos limites inferiores e superiores globais têm a ser definido. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Coment�rios

Provedores de serviços de chamarem o método de **IMAPIProgress::SetLimits** para definir ou limpar o sinalizador MAPI_TOP_LEVEL e para definir os valores máximo e mínimo de globais e locais. O valor da configuração de sinalizador afeta se o objeto de progresso entende os valores mínimos e máximo para ser local ou global. Quando o sinalizador MAPI_TOP_LEVEL estiver definido, esses valores são considerados globais e são usados para calcular o progresso de toda a operação. Objetos de progresso inicializar o valor mínimo global como 1 e o valor máximo global a 1000. 
  
Quando MAPI_TOP_LEVEL não estiver definida, os valores mínimos e máximo são considerados locais e provedores de usá-los internamente para exibir o progresso de subobjetos de nível inferiores. Objetos de progresso salvar os valores mínimos e máximo locais somente para que pode ser retornados para provedores quando os métodos [IMAPIProgress::GetMin](imapiprogress-getmin.md) e [IMAPIProgress::GetMax](imapiprogress-getmax.md) são chamados. 
  
Para obter mais informações sobre como implementar **SetLimits** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::SetLimits  <br/> |MFCMAPI usa o método **IMAPIProgress::SetLimits** para definir os sinalizadores para o objeto de progresso e limites máximo e mínimos.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress: IUnknown](imapiprogressiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Implementando um indicador de progresso](implementing-a-progress-indicator.md)

