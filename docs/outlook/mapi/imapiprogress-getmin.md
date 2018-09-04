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
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587821"
---
# <a name="imapiprogressgetmin"></a>IMAPIProgress::GetMin

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o valor mínimo no método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) cujas informações do progresso são exibidas. 
  
```cpp
HRESULT GetMin(
  ULONG FAR * lpulMin
);
```

## <a name="parameters"></a>Parâmetros

 _lpulMin_
  
> [out] Um ponteiro para o número mínimo de itens na operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O número mínimo de itens na operação foi recuperado.
    
## <a name="remarks"></a>Comentários

O valor mínimo representa o início da operação em formato numérico. O valor pode ser um valor máximo global, usado para representar o escopo de toda a exibição do progresso, ou um valor local, usado para representar apenas uma parte da exibição. 
  
O valor da configuração do sinalizador afeta se o objeto de progresso entende o valor mínimo como local ou global. Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor mínimo será considerado como global e usado para calcular o progresso de toda a operação. Quando MAPI_TOP_LEVEL não estiver definido, o valor mínimo será considerado como local, e os provedores o usam internamente para exibir o progresso de subobjetos de níveis inferiores. Os objetos de progresso salvam o valor mínimo local apenas para retorná-lo a um provedor por meio de uma chamada **GetMin**. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Inicialize o valor mínimo como 1. Para redefinir esse valor, os provedores de serviços podem chamar o método **IMAPIProgress::SetLimits**. Para saber mais sobre como implementar **GetMin** e os outros métodos [IMAPIProgress](imapiprogressiunknown.md), confira [Como implementar um indicador de progresso](implementing-a-progress-indicator.md).
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMin  <br/> |O MFCMAPI usa o método **IMAPIProgress::GetMin** para obter o valor mínimo do indicador de progresso. Retorna 1, a menos que os limites tenham sido definidos anteriormente chamando o método **IMAPIProgress::SetLimits**.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMax](imapiprogress-getmax.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

