---
title: IProviderAdminDeleteProvider
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProviderAdmin.DeleteProvider
api_type:
- COM
ms.assetid: 0065b50f-95f6-4af1-81c2-a73e5111eecf
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 28dbbb98c9810bb688b9ecdd730ef6c4ada5f60b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404859"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um provedor de serviços do serviço de mensagens.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in, out] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser excluído. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor foi excluído com êxito do serviço de mensagens.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado pelo parâmetro  _lpUID_ não foi reconhecido. 
    
## <a name="remarks"></a>Comentários

O **método IProviderAdmin::D eleteProvider** exclui um provedor de serviços do serviço de mensagens. **DeleteProvider** determina o provedor de serviços a ser excluído correspondendo a estrutura **MAPIUID** apontada por  _lpUID_ com o conjunto de identificadores registrados pelos provedores de serviços ativos. 
  
A maioria dos serviços de mensagens não permite que provedores sejam excluídos enquanto o perfil estiver em uso. Se o provedor a ser excluído estiver em uso, **DeleteProvider** marca-o para exclusão em vez de removê-lo imediatamente e retorna S_OK. Quando o provedor não está mais sendo usado, ele é excluído. 
  
 **DeleteProvider** chama a função de ponto de entrada do serviço de mensagens antes que o provedor seja removido do serviço. O  _parâmetro ulContext_ é definido como MSG_SERVICE_PROVIDER_DELETE. A função de ponto de entrada do serviço de mensagens executa as seguintes tarefas: 
  
- Exclui o provedor de serviços.
    
- Exclui a seção de perfil do provedor de serviços.
    
A função de ponto de entrada do serviço de mensagens não é chamada novamente depois que o provedor é excluído.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

