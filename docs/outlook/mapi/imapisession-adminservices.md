---
title: IMAPISessionAdminServices
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.AdminServices
api_type:
- COM
ms.assetid: 487fab39-5c2c-4e1a-9f90-4da64f5e198b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cb7fa7bb7dc17a89fc7cc40ae370accc40fa3941
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579834"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro [IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações em serviços de mensagens. 
  
```cpp
HRESULT AdminServices(
  ULONG ulFlags,
  LPSERVICEADMIN FAR * lppServiceAdmin
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lppServiceAdmin_
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do serviço de mensagem.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Um ponteiro para um objeto de administração do serviço de mensagem foi retornado com êxito.
    
## <a name="notes-to-callers"></a>Notas para chamadores

O método **IMAPISession::AdminServices** cria um objeto de administração do serviço de mensagem, um objeto que dá suporte à interface **IMsgServiceAdmin** e retorna um ponteiro. Usando esse ponteiro, você pode chamar métodos de **IMsgServiceAdmin** para alterar qualquer um dos serviços de mensagem no perfil da sessão. Lembre-se de que essas alterações não terão efeito até a sessão seguinte; a sessão atual não é afetada. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI usa o método **IMAPISession::AdminServices** para acessar o perfil para ler o nome do servidor.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

