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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c7124c8e3f2ced66d303321ff7aee8592a723a2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420238"
---
# <a name="iprofadminchangeprofilepassword"></a>IProfAdmin::ChangeProfilePassword

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Depreciado. Altera a senha de um perfil.
  
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
  
> [in] Um ponteiro para o nome do perfil associado à senha a ser alterada.
    
 _lpszOldPassword_
  
> [in] Um ponteiro para a senha atual.
    
 _lpszNewPassword_
  
> [in] Um ponteiro para a nova senha.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o tipo das cadeias de caracteres passadas. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> O nome do perfil e as senhas estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, essas cadeias de caracteres estão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Se esse método for chamado, ele retornará S_OK. No entanto, nenhuma ação será tomada.
    
## <a name="remarks"></a>Comentários

Não use esse método. O MAPI não dá suporte a senhas para perfis.
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

