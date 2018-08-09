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
ms.openlocfilehash: 8964ba8c4341bec431bdbc1690d639b345df8b1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767126"
---
# <a name="imapiprogressgetflags"></a>IMAPIProgress::GetFlags

  
  
**Aplica-se a**: Outlook 
  
Retorna sinaliza as configurações do objeto de andamento para o nível de operação no qual as informações sobre o andamento é calculado.
  
```cpp
HRESULT GetFlags(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpulFlags_
  
> [out] Uma bitmask dos sinalizadores que controla o nível de operação em andamento da qual as informações são calculadas. O seguinte sinalizador pode ser retornado:
    
MAPI_TOP_LEVEL 
  
> Progresso está sendo calculado para o objeto de nível superior, o objeto que é chamado pelo cliente para iniciar a operação. Por exemplo, o objeto de nível superior em uma operação de cópia da pasta é a pasta que está sendo copiada. Quando MAPI_TOP_LEVEL não estiver definida, o progresso é calculado para um objeto de nível inferior ou subobjeto. Na operação de cópia de pasta, um objeto de nível inferior é uma das subpastas na pasta que está sendo copiada.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O valor flags foi retornado com êxito.
    
## <a name="remarks"></a>Comentários

MAPI permite que os provedores de serviço diferenciar entre objetos de nível superior e subobjetos com o sinalizador MAPI_TOP_LEVEL para que todos os objetos envolvidos em uma operação podem usar a mesma implementação [IMAPIProgress](imapiprogressiunknown.md) para mostrar o progresso. Isso faz com que a exibição de indicador prossiga normalmente em uma única direção positiva. Se o sinalizador MAPI_TOP_LEVEL está definido determina como provedores de serviços de definir os outros parâmetros em chamadas subsequentes ao objeto de andamento. 
  
O valor retornado pela **GetFlags** é definido inicialmente pelo implementador e subsequentemente pelo provedor de serviços através de uma chamada ao método [IMAPIProgress::SetLimits](imapiprogress-setlimits.md) . 
  
## <a name="notes-to-implementers"></a>Notas para implementadores

Sempre inicializar o sinalizador para MAPI_TOP_LEVEL e depois contam com provedores de serviços para desmarcá-la quando apropriado. Provedores de serviços podem desmarcar e redefinir o sinalizador chamando o método **IMAPIProgress::SetLimits** . Para obter mais informações sobre como implementar **GetFlags** e outros métodos **IMAPIProgress** , consulte [Implementando um indicador de progresso](implementing-a-progress-indicator.md).
  
## <a name="notes-to-callers"></a>Notas para chamadores

Quando você exibe um indicador de progresso, faça uma chamada para **IMAPIProgress::GetFlags**para sua primeira chamada. O valor retornado deve ser MAPI_TOP_LEVEL, porque todas as implementações inicializar o conteúdo do parâmetro _lpulFlags_ para esse valor. Para obter mais informações sobre a sequência de chamadas para um objeto de progresso, consulte [Exibir um indicador de progresso](how-to-display-a-progress-indicator.md).
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIProgress.cpp  <br/> |CMAPIProgress::GetFlags  <br/> |MFCMAPI usa o método **IMAPIProgress::GetFlags** para determinar quais sinalizadores estão definidos. Retorna MAPI_TOP_LEVEL, a menos que foram configuradas usando o método **IMAPIProgress::SetLimits** .  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIProgress::SetLimits](imapiprogress-setlimits.md)
  
[IMAPIProgress : IUnknown](imapiprogressiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)
  
[Exibir um indicador de progresso](how-to-display-a-progress-indicator.md)
  
[Implementar um indicador de progresso](implementing-a-progress-indicator.md)

