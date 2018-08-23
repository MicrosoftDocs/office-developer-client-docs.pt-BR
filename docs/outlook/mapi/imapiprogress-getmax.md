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
ms.openlocfilehash: 2dadad410b9aaf1401d792de373e561c29183a12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567234"
---
# <a name="imapiprogressgetmax"></a>IMAPIProgress::GetMax

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o número máximo de itens na operação para o qual andamento informações são exibidas.
  
```cpp
HRESULT GetMax(
  ULONG FAR * lpulMax
);
```

## <a name="parameters"></a>Parâmetros

 _lpulMax_
  
> [out] Um ponteiro para o número máximo de itens na operação.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O número máximo de itens na operação terem sido recuperado.
    
## <a name="remarks"></a>Comentários

O valor máximo representa o fim da operação no formulário numérico. O valor pode ser um valor máximo global, usado para representar o escopo da tela inteira progresso, ou um valor local, usado para representar a apenas uma parte da tela. 
  
O valor da configuração de sinalizador afeta se o objeto de progresso entende o valor máximo seja local ou global. Quando o sinalizador MAPI_TOP_LEVEL estiver definido, o valor máximo é considerado como global e é usado para calcular o progresso de toda a operação. Quando MAPI_TOP_LEVEL não estiver definida, o valor máximo é considerado como local e provedores usam internamente para exibir o progresso subobjetos de nível inferiores. Objetos de progresso salvar o valor máximo local somente para retorná-lo a um provedor através de uma chamada **GetMax** . 
  
Para obter mais informações sobre como e quando fazer chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Inicialize o valor máximo a 1000. Provedores de serviços podem redefinir esse valor chamando o método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . Para obter mais informações sobre como implementar **GetMax** e outros métodos [IMAPIProgress](imapiprogressiunknown.md) , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetMax  <br/> |MFCMAPI usa o método **IMAPIProgress::GetMax** para obter o valor máximo para o objeto de andamento. Retorna a 1000, a menos que limites anteriormente foram definidos com o método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::GetMin](imapiprogress-getmin.md)
  
[IMAPIProgress::Progress](imapiprogress-progress.md)
  
[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Implementar um indicador de progresso](implementing-a-progress-indicator.md)

