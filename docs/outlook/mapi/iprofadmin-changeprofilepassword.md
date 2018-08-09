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
ms.openlocfilehash: c57f945d16cc80c637b1a4074b25f9cf1fb1edc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767630"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Aplica-se a**: Outlook 
  
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

