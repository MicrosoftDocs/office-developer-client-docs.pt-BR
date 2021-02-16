---
title: IProfAdminCopyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.CopyProfile
api_type:
- COM
ms.assetid: f4846dc3-0236-44ed-a1b1-8c13d48fb58a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: c3c4ac10003aad8949de94e0f144410af10078b1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437235"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Copia um perfil.
  
```cpp
HRESULTCopyProfile(
  LPSTR lpszOldProfileName,
  LPSTR lpszOldPassword,
  LPSTR lpszNewProfileName,
  ULONG_PTR ulUIParam,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpszOldProfileName_
  
> [in] Um ponteiro para o nome do perfil a ser copiado.
    
 _lpszOldPassword_
  
> [in] Um ponteiro para a senha do perfil a ser copiado.
    
 _lpszNewProfileName_
  
> [in] Um ponteiro para o novo nome do perfil copiado.
    
 _ulUIParam_
  
> [in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o perfil é copiado. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo que solicita ao usuário a senha correta do perfil a ser copiado. Se esse sinalizador não estiver definido, nenhuma caixa de diálogo será exibida.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O perfil foi copiado com êxito.
    
MAPI_E_ACCESS_DENIED 
  
> O novo nome de perfil é o mesmo de um perfil existente.
    
MAPI_E_LOGON_FAILED 
  
> A senha para o perfil a ser copiado está incorreta e uma caixa de diálogo não pôde ser exibida para o usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido no _parâmetro ulFlags._ 
    
MAPI_E_NOT_FOUND 
  
> O perfil especificado não existe.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, normalmente clicando no botão Cancelar **em** uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O **método IProfAdmin::CopyProfile** faz uma cópia do perfil apontado por  _lpszOldProfileName_, dando a ele o nome apontado por  _lpszNewProfileName_. Copiar um perfil deixa a cópia com a mesma senha do original.
  
O nome do perfil original, sua senha e a cópia podem ter até 64 caracteres e podem incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo caracteres de ênfase e o caractere de sublinhado.
    
- Espaços incorporados, mas não espaços à frente ou à frente.
    
Não há suporte para senhas de perfil em todos os sistemas operacionais. Em sistemas operacionais que não suportam senhas de perfil,  _lpszOldPassword_ pode ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
Se  _lpszOldPassword_ for definido como NULL, o perfil a ser copiado exigirá uma senha e o sinalizador MAPI_DIALOG definido; uma caixa de diálogo que solicita que o usuário forneça a senha é exibida. Se uma senha for necessária, mas  _lpszOldPassword_ for definida como NULL e o sinalizador MAPI_DIALOG não estiver definido, **CopyProfile** retornará MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

