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
ms.openlocfilehash: c639523a02047bf00c378dafd7bc698d7d4e5fff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405902"
---
# <a name="imapisessionadminservices"></a>IMAPISession::AdminServices

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um [ponteiro IMsgServiceAdmin](imsgserviceadminiunknown.md) para fazer alterações nos serviços de mensagens. 
  
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
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do serviço de mensagens.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Um ponteiro para um objeto de administração do serviço de mensagens foi retornado com êxito.
    
## <a name="notes-to-callers"></a>Notas para chamadores

O **método IMAPISession::AdminServices** cria um objeto de administração de serviço de mensagens, um objeto que oferece suporte à interface **IMsgServiceAdmin** e retorna um ponteiro. Usando esse ponteiro, você pode chamar métodos **IMsgServiceAdmin** para alterar qualquer um dos serviços de mensagem no perfil de sessão. Esteja ciente de que essas alterações não têm efeito até a próxima sessão; a sessão atual não é afetada. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIStoreFunctions.cpp  <br/> |GetServerName  <br/> |MFCMAPI usa o **método IMAPISession::AdminServices** para acessar o perfil para ler o nome do servidor.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)
  
[IProfAdmin::AdminServices](iprofadmin-adminservices.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

