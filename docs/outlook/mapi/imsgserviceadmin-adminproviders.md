---
title: IMsgServiceAdminAdminProviders
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.AdminProviders
api_type:
- COM
ms.assetid: 0d605e2c-10db-46e1-95d5-12fabd524baa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6b7360995a781824b50ff02b5d2dec8e481e7ba7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422758"
---
# <a name="imsgserviceadminadminproviders"></a>IMsgServiceAdmin::AdminProviders

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna um ponteiro que fornece acesso a um objeto de administração do provedor.
  
```cpp
HRESULT AdminProviders(
  LPMAPIUID lpUID,
  ULONG ulFlags,
  LPPROVIDERADMIN FAR * lppProviderAdmin
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagens a ser administrado. 
    
 _ulFlags_
  
> [in] Sempre NULO. 
    
 _lppProviderAdmin_
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do provedor.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto de administração do provedor foi retornado com êxito.
    
MAPI_E_NOT_FOUND 
  
> O **MAPIUID** apontado por  _lpUID_ não existe. 
    
## <a name="remarks"></a>Comentários

O **método IMsgServiceAdmin::AdminProviders** fornece acesso a um objeto de administração do provedor. A administração de um provedor é um objeto que dá suporte à interface [IProviderAdmin](iprovideradminiunknown.md) e permite que os clientes faça o seguinte: 
  
- Adicione provedores de serviços a um serviço de mensagens.
    
- Exclua provedores de serviços de um serviço de mensagens.
    
- Abra seções de perfil.
    
- Acessar a tabela do provedor de serviços de mensagens.
    
Os tipos de alterações que podem realmente ser feitas em um serviço de mensagens enquanto o perfil está em uso dependem do serviço de mensagens. No entanto, a maioria dos serviços de mensagens não suporta alterações como adicionar e excluir provedores enquanto o perfil estiver em uso.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** para o serviço de mensagens administrar, recupere a coluna da propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagens na tabela de serviço de mensagens. Para obter mais informações, consulte o procedimento descrito no [método IMsgServiceAdmin::CreateMsgService.](imsgserviceadmin-createmsgservice.md) 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa o **método IMsgServiceAdmin::AdminProviders** para abrir um objeto de administração de provedor para um serviço.  <br/> |
   
## <a name="see-also"></a>Confira também



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

