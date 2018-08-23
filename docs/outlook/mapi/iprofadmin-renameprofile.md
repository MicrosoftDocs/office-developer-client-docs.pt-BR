---
title: IProfAdminRenameProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.RenameProfile
api_type:
- COM
ms.assetid: 2a575cac-dbfd-4f42-9c10-4b7e355a065e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4453465c04d7a5a3de79f2ae34d13095863487cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569502"
---
# <a name="iprofadminrenameprofile"></a>IProfAdmin::RenameProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Atribui um novo nome a um perfil.
  
```cpp
HRESULT RenameProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszOldProfileName_
  
> [in] Um ponteiro para o nome atual do perfil para renomear.
    
 _lpszOldPassword_
  
> [in] Sempre nulo.
    
 _lpszNewProfileName_
  
> [in] Um ponteiro para o novo nome do perfil para renomear.
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe. 
    
 _ulFlags_
  
> [in] Sempre nulo.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O perfil foi renomeado com êxito.
    
MAPI_E_LOGON_FAILED 
  
> A senha do perfil está incorreta.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::RenameProfile** atribui um novo nome para um perfil, caso haja algum. Se o perfil renomear estiver sendo usado por um cliente quando **RenameProfile** é chamado, o **RenameProfile** marca o perfil e retorna S_OK em vez de tentar a operação de renomeação enquanto o perfil estiver em uso. Quando o perfil não mais estiver sendo usado, **RenameProfile** atribui o novo nome. 
  
Os nomes antigos e novos do perfil podem ter até 64 caracteres de comprimento e podem incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
O _lpszPassword_ deve sempre ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

