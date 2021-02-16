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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 162f20485fc21cf8523b6d4a653e52c35f4b3d9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419517"
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
  
> [in] Um ponteiro para o nome atual do perfil a ser renomedo.
    
 _lpszOldPassword_
  
> [in] Sempre NULO.
    
 _lpszNewProfileName_
  
> [in] Um ponteiro para o novo nome do perfil a ser renomedo.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe. 
    
 _ulFlags_
  
> [in] Sempre NULO.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O perfil foi renomeado com êxito.
    
MAPI_E_LOGON_FAILED 
  
> A senha do perfil está incorreta.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IProfAdmin::RenameProfile** atribui um novo nome a um perfil, se tiver um. Se o perfil a ser renomeado estiver sendo usado por um cliente quando **RenameProfile** for chamado, **RenameProfile** marcará o perfil e retornará S_OK em vez de tentar renomear a operação enquanto o perfil estiver em uso. Quando o perfil não está mais sendo usado, **RenameProfile** atribui a ele o novo nome. 
  
Os nomes antigo e novo do perfil podem ter até 64 caracteres e podem incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.
    
- Espaços incorporados, mas não espaços à frente ou à frente.
    
O  _lpszPassword_ sempre deve ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

