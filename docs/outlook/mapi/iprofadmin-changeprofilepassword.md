---
title: IProfAdminChangeProfilePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.ChangeProfilePassword
api_type:
- COM
ms.assetid: a41f707a-5c84-49aa-aeb6-469b2600e181
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 41066d4418760a676fbc02241bfc12d83275da9d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572995"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obsoleto. Altera a senha de um perfil.
  
```cpp
HRESULT ChangeProfilePassword(
  LPSTR lpszProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewPassword,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszProfileName_
  
> [in] Um ponteiro para o nome do perfil associado a senha a ser alterado.
    
 _lpszOldPassword_
  
> [in] Um ponteiro para a senha atual.
    
 _lpszNewPassword_
  
> [in] Um ponteiro para a nova senha.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo das cadeias de caracteres no passado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> O nome do perfil e senhas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Se esse método for chamado, ela retornará S_OK. No entanto, nenhuma ação será tomada.
    
## <a name="remarks"></a>Comentários

Não use esse método. MAPI não suporta senhas para perfis.
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

