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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: db09b44bd8eeeb3ab56513b1b9c2cab69f776002
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590082"
---
# <a name="iprovideradmindeleteprovider"></a>IProviderAdmin::DeleteProvider

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Exclui um provedor de serviço do serviço de mensagem.
  
```cpp
HRESULT DeleteProvider(
  LPMAPIUID lpUID
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [além, out] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser excluído. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O provedor foi excluído com êxito do serviço de mensagem.
    
E_NOT_FOUND 
  
> **MAPIUID** apontado pelo parâmetro _lpUID_ não foi reconhecido. 
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::DeleteProvider** exclui um provedor de serviço do serviço de mensagem. **DeleteProvider** determina o provedor de serviços para excluir combinando a estrutura **MAPIUID** apontada pela _lpUID_ com o conjunto de identificadores registrados pelos provedores de serviço ativo. 
  
A maioria dos serviços de mensagem não permita provedores a ser excluída enquanto o perfil estiver em uso. Se o provedor para excluir estiver em uso, **DeleteProvider** marca para exclusão, em vez de removê-lo imediatamente e retorna S_OK. Quando o provedor não está sendo usado, ela é excluída. 
  
 **DeleteProvider** chama a função de ponto de entrada do serviço de mensagem antes que o provedor é removido do serviço de. O parâmetro _ulContext_ é definido como MSG_SERVICE_PROVIDER_DELETE. A função de ponto de entrada de serviço de mensagem executa as seguintes tarefas: 
  
- Exclui o provedor de serviço.
    
- Exclui a seção de perfil do provedor de serviços.
    
A função de ponto de entrada de serviço de mensagem não é chamada novamente após o provedor ter sido excluído.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

