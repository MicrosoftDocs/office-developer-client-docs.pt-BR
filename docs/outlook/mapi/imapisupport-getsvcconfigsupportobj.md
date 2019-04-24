---
title: IMAPISupportGetSvcConfigSupportObj
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetSvcConfigSupportObj
api_type:
- COM
ms.assetid: 56c3bdae-a3a8-4334-b6d2-a89c6820d72e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 6de0fed4df9d23e67c3520ffb019a961b890f988
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316552"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria um objeto de suporte de serviço de mensagens.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _lppSvcSupport_
  
> bota Um ponteiro para um ponteiro para o novo objeto de suporte do serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de suporte de configuração foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: GetSvcConfigSupportObj** é implementado para todos os objetos de suporte. Os provedores de serviços chamam o **GetSvcConfigSupportObj** para criar um objeto de suporte de configuração para passar para uma função de ponto de entrada de serviço de mensagens. 
  
Uma função de ponto de entrada de serviço de mensagem é baseada no protótipo [MSGSERVICEENTRY](msgserviceentry.md) e é chamada por métodos da interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Uma função de ponto de entrada de serviço de mensagens permite que os serviços de mensagens configurem-se ou realizem outras ações quando o perfil é alterado. As funções de ponto de entrada de serviço de mensagens podem suportar alterações de configuração exibindo uma folha de propriedades ou por meio de uma matriz de valor de propriedade passada para o método [IMsgServiceAdmin:: ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

