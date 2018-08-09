---
title: IProfAdminSetDefaultProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.SetDefaultProfile
api_type:
- COM
ms.assetid: 58f50535-b0ed-4097-bda8-fd3ccc2d4b49
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cf5060ba2113032fe1e13e5417590006808a53e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767629"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Aplica-se a**: Outlook 
  
Define ou limpa o perfil padrão de um cliente.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil que será se tornam o padrão ou NULL. A definição de _lpszProfileName_ como nulo indica que o **SetDefaultProfile** deve remover o perfil padrão existente, deixando o cliente sem um padrão. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo da cadeia de caracteres apontado pela _lpszProfileName_. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O nome do perfil está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome de perfil é no formato ANSI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Um perfil padrão foi estabelecido ou removido com êxito.
    
E_NOT_FOUND 
  
> O perfil especificado não existe.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::SetDefaultProfile** estabelece um perfil específico como o perfil do cliente padrão ou limpa o perfil padrão atual. O perfil padrão é o perfil que será usado automaticamente sempre que o cliente inicia uma sessão MAPI. **SetDefaultProfile** também define a propriedade de **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) do novo perfil padrão como TRUE.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para iniciar uma sessão com o perfil padrão, passe o sinalizador MAPI_USE_DEFAULT para a função [MAPILogonEx](mapilogonex.md) . 
  
## <a name="see-also"></a>Confira também



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriedade canônica PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

