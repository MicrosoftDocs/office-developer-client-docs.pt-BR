---
title: IMAPIProgressGetMin
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMin
api_type:
- COM
ms.assetid: caceddf1-0f7c-47b5-97bf-17ffe3440a6c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cff866ce73eb6ada45a2b629a6c95c69ad189045
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587821"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o valor mínimo no método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) para qual andamento informações são exibidas. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parâmetros

 _lpulMin_
  
> [out] Um ponteiro para o número mínimo de itens na operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O número mínimo de itens na operação terem sido recuperado.
    
## <a name="remarks"></a>Comentários

O valor mínimo representa o início da operação no formulário numérico. O valor pode ser um valor máximo global, usado para representar o escopo da tela inteira progresso, ou um valor local, usado para representar a apenas uma parte da tela. 
  
O valor da configuração de sinalizador afeta se o objeto de progresso entende o valor mínimo seja local ou global. Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor mínimo é considerado como global e é usado para calcular o progresso de toda a operação. Quando MAPI_TOP_LEVEL não estiver definida, o valor mínimo é considerado local e provedores usam internamente para exibir o progresso subobjetos de nível inferiores. Objetos de progresso salvar o valor mínimo local somente para retorná-lo a um provedor através de uma chamada **GetMin** . 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Inicialize o valor mínimo como 1. Provedores de serviços podem redefinir esse valor chamando o método **IMAPIProgress::SetLimits** . Para obter mais informações sobre como implementar **GetMin** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |MFCMAPI usa o método **IMAPIProgress::GetMin** para obter o valor mínimo para o indicador de progresso. Retornará 1, a menos que limites tenham sido definidos anteriormente chamando o método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Implementar um indicador de progresso](implementing-a-progress-indicator.md)

