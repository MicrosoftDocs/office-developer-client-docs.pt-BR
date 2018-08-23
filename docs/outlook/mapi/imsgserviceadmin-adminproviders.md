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
ms.openlocfilehash: 1b03245d7af4c6fb3879e597d8345e5d9888e164
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567206"
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
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que contém o identificador exclusivo para o serviço de mensagem a serem administrados. 
    
 _ulFlags_
  
> [in] Sempre nulo. 
    
 _lppProviderAdmin_
  
> [out] Um ponteiro para um ponteiro para um objeto de administração do provedor.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto de administração do provedor foi retornado com êxito.
    
E_NOT_FOUND 
  
> **MAPIUID** apontado pela _lpUID_ não existe. 
    
## <a name="remarks"></a>Comentários

O método **IMsgServiceAdmin::AdminProviders** fornece acesso a um objeto de administração do provedor. A administração de um provedor é um objeto que dá suporte à interface [IProviderAdmin](iprovideradminiunknown.md) e permite que os clientes façam o seguinte: 
  
- Adicione provedores de serviço para um serviço de mensagem.
    
- Exclua provedores de serviço de um serviço de mensagem.
    
- Abrir seções de perfil.
    
- Acesse a tabela de provedor de serviços de mensagem.
    
Os tipos de alterações que realmente podem ser feitas para um serviço de mensagem enquanto o perfil estiver em uso dependem do serviço de mensagem. No entanto, a maioria dos serviços de mensagem não suportam alterações como adicionar e excluir provedores enquanto o perfil estiver em uso.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para recuperar a estrutura **MAPIUID** para administrar o serviço de mensagem, recupere a coluna de propriedade **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) da linha do serviço de mensagem da tabela de serviço de mensagem. Para obter mais informações, consulte o procedimento descrito no método [IMsgServiceAdmin:: CreateMsgService](imsgserviceadmin-createmsgservice.md) . 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MsgServiceTableDlg.cpp  <br/> |CMsgServiceTableDlg::OnDisplayItem  <br/> |MFCMAPI usa o método **IMsgServiceAdmin::AdminProviders** para abrir um objeto de administração do provedor de um serviço.  <br/> |
   
## <a name="see-also"></a>Confira também



[IProviderAdmin : IUnknown](iprovideradminiunknown.md)
  
[MAPIUID](mapiuid.md)
  
[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

