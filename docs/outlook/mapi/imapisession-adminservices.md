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
ms.openlocfilehash: 850d4d952102e11d11234fa3184b88e280a98c21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767194"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Aplica-se a**: Outlook 
  
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

