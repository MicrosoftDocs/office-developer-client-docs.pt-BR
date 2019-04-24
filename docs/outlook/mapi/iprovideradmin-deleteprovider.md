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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279546"
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
  
> [in, out] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo que representa o provedor a ser excluído. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O provedor foi excluído com êxito do serviço de mensagens.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado pelo parâmetro _lpUID_ não foi reconhecido. 
    
## <a name="remarks"></a>Comentários

O método **IProviderAdmin::D eleteprovider** exclui um provedor de serviços do serviço de mensagens. **Deleteprovider** determina o provedor de serviços a ser excluído combinando a estrutura **MAPIUID** indicada por _lpUID_ com o conjunto de identificadores registrados pelos provedores de serviços ativos. 
  
A maioria dos serviços de mensagem não permite que os provedores sejam excluídos enquanto o perfil está em uso. Se o provedor a ser excluído estiver em uso **** , o deleteprovider o marcará para exclusão em vez de removê-lo imediatamente e retornará S_OK. Quando o provedor não está mais sendo usado, ele é excluído. 
  
 **Deleteprovider** chama a função de ponto de entrada do serviço de mensagem antes de o provedor ser removido do serviço. O parâmetro _ulContext_ é definido como MSG_SERVICE_PROVIDER_DELETE. A função de ponto de entrada do serviço de mensagens realiza as seguintes tarefas: 
  
- Exclui o provedor de serviços.
    
- Exclui a seção de perfil do provedor de serviços.
    
A função de ponto de entrada do serviço de mensagem não é chamada novamente após o provedor ter sido excluído.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IProviderAdmin : IUnknown](iprovideradminiunknown.md)

