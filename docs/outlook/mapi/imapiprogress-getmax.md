---
title: IMAPIProgressGetMax
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetMax
api_type:
- COM
ms.assetid: 88a910ed-b55a-4e5b-a43d-eb3ea795a70e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 64b6235151c7700a24992bc1d4394553a53c0464
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436199"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o número máximo de itens na operação para o qual as informações de progresso são exibidas.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parâmetros

 _lpulMax_
  
> bota Um ponteiro para o número máximo de itens na operação.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O número máximo de itens na operação foi recuperado.
    
## <a name="remarks"></a>Comentários

O valor máximo representa o fim da operação em formato numérico. O valor pode ser um valor máximo global, usado para representar o escopo de toda a exibição do progresso, ou um valor local, usado para representar apenas uma parte da exibição. 
  
O valor da configuração do sinalizador afeta se o objeto Progress entende o valor máximo como local ou global. Quando o sinalizador MAPI_TOP_LEVEL é definido, o valor máximo é considerado como global e é usado para calcular o progresso de toda a operação. Quando MAPI_TOP_LEVEL não é definido, o valor máximo é considerado como local e os provedores o utilizam internamente para exibir o progresso de subobjetos de nível inferior. Os objetos Progress salvam o valor máximo local somente para devolvê-lo a um provedor por meio de uma chamada **GetMax** . 
  
Para saber mais sobre como e quando fazer chamadas para um objeto de progresso, confira o tópico [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Inicialize o valor máximo para 1000. Para redefinir esse valor, os provedores de serviços podem chamar o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md). Para obter mais informações sobre como implementar o **GetMax** e os outros métodos do [método imapiprogress](imapiprogressiunknown.md) , consulte [implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: GetMax  <br/> |MFCMAPI usa o método **método imapiprogress:: GetMax** para obter o valor máximo para o objeto Progress. Retorna 1000, a menos que os limites tenham sido definidos anteriormente com o método **método imapiprogress::** setlimits.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

