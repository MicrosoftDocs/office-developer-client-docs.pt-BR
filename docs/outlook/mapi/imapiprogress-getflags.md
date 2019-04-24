---
title: IMAPIProgressGetFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProgress.GetFlags
api_type:
- COM
ms.assetid: 7af74fcc-c0df-4f58-a2d4-0a79c96b2e81
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 810192bfc85c9934a282f02a0839aaed539f744d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270264"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna as configurações de sinalizador do objeto Progress para o nível de operação em que as informações de progresso são calculadas.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> bota Uma bitmask de sinalizadores que controla o nível de operação no qual as informações de progresso são calculadas. O seguinte sinalizador pode ser retornado:
    
MAPI_TOP_LEVEL 
  
> O andamento é calculado para o objeto de nível superior, o objeto que é chamado pelo cliente para iniciar a operação. Por exemplo, o objeto de nível superior em uma operação de cópia de pasta é a pasta que está sendo copiada. Quando MAPI_TOP_LEVEL não é definido, o andamento é calculado para um objeto de nível inferior ou subobjeto. Na operação de cópia de pasta, um objeto de nível inferior é uma das subpastas na pasta que está sendo copiada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O valor do sinalizador foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

O MAPI permite que os provedores de serviços diferenciem entre objetos de nível superior e subobjetos com o sinalizador MAPI_TOP_LEVEL para que todos os objetos envolvidos em uma operação possam usar a mesma implementação do [método imapiprogress](imapiprogressiunknown.md) para mostrar o progresso. Isso faz com que o indicador seja exibido tranqüilamente em uma única direção positiva. Se o sinalizador MAPI_TOP_LEVEL é definido determina como os provedores de serviços definem os outros parâmetros nas chamadas subsequentes para o objeto Progress. 
  
O valor retornado por **GetFlags** é definido inicialmente pelo implementador e subsequentemente pelo provedor de serviços por meio de uma chamada para o método [método imapiprogress::](imapiprogress-setlimits.md) setlimits. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Sempre inicialize o sinalizador para MAPI_TOP_LEVEL e, em seguida, confie nos provedores de serviço para desmarcá-lo quando for apropriado. Os provedores de serviços podem limpar e redefinir o sinalizador chamando o método **método imapiprogress::** setlimits. Para obter mais informações sobre como implementar **GetFlags** e os outros métodos do **método imapiprogress** , consulte [implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Ao exibir um indicador de progresso, faça sua primeira chamada para **método imapiprogress:: GetFlags**. O valor retornado deve ser MAPI_TOP_LEVEL, pois todas as implementações inicializam o conteúdo do parâmetro _lpulFlags_ para esse valor. Para obter mais informações sobre a sequência de chamadas para um objeto Progress, consulte [exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress:: getFlags  <br/> |MFCMAPI usa o método **método imapiprogress:: GetFlags** para determinar quais sinalizadores estão definidos. Retorna MAPI_TOP_LEVEL a menos que sinalizadores tenham sido definidos usando o método **método imapiprogress::** setlimits.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Como implementar um indicador de progresso](implementing-a-progress-indicator.md)

