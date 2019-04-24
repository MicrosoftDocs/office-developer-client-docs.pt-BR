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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 44be43864d943257520f27297e5754a4978c568d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32270165"
---
# <a name="iprofadminsetdefaultprofile"></a>IProfAdmin::SetDefaultProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define ou limpa o perfil padrão de um cliente.
  
```cpp
HRESULT SetDefaultProfile(
  LPSTR lpszProfileName,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> no Um ponteiro para o nome do perfil que se tornará o padrão, ou nulo. Definir _lpszProfileName_ como nulo indica que o **setdefaultprofile foi** deve remover o perfil padrão existente, deixando o cliente sem um padrão. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo da cadeia de caracteres indicada por _lpszProfileName_. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O nome do perfil está no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, o nome do perfil estará no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Um perfil padrão foi estabelecido ou removido com êxito.
    
MAPI_E_NOT_FOUND 
  
> O perfil especificado não existe.
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin:: setdefaultprofile foi** estabelece um perfil específico como o perfil padrão do cliente ou limpa o perfil padrão atual. O perfil padrão é o perfil que é usado automaticamente sempre que o cliente inicia uma sessão MAPI. **Setdefaultprofile foi** também define a propriedade **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) do novo perfil padrão como true.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para iniciar uma sessão com o perfil padrão, passe o sinalizador MAPI_USE_DEFAULT para a função [funçãomapilogonex](mapilogonex.md) . 
  
## <a name="see-also"></a>Confira também



[IProfAdmin::GetProfileTable](iprofadmin-getprofiletable.md)
  
[MAPILogonEx](mapilogonex.md)
  
[Propriedade canônica PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)

