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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5d7e3e89f15b1bc08c7ce9faab0d0a6326300e70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767232"
---
# <a name="imapisupportgetsvcconfigsupportobj"></a>IMAPISupport::GetSvcConfigSupportObj

  
  
**Aplica-se a**: Outlook 
  
Cria um objeto de suporte de serviço de mensagem.
  
```cpp
HRESULT GetSvcConfigSupportObj(
  ULONG ulFlags,
  LPMAPISUP FAR * lppSvcSupport
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lppSvcSupport_
  
> [out] Um ponteiro para um ponteiro para o novo objeto de suporte de serviço de mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto de configuração de suporte foi criado com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::GetSvcConfigSupportObj** é implementado para todos os objetos de suporte. Provedores de serviços de chamarem **GetSvcConfigSupportObj** para criar um objeto de configuração de suporte a serem passados para uma função de ponto de entrada de serviço de mensagens. 
  
Uma função de ponto de entrada de serviço de mensagem se baseia em protótipo [MSGSERVICEENTRY](msgserviceentry.md) e é chamada pelo métodos da interface [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Uma função de ponto de entrada de serviço de mensagens permite que os serviços de mensagens configurar sozinhos ou executar outras ações quando o perfil é alterado. Ponto de entrada de serviço de mensagem funções podem suportar as alterações de configuração, exibindo uma folha de propriedades ou por meio de uma matriz de valores de propriedade é passado para o método [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md) . 
  
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md)
  
[IMsgServiceAdmin::CreateMsgService](imsgserviceadmin-createmsgservice.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)
  
[MSGSERVICEENTRY](msgserviceentry.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

