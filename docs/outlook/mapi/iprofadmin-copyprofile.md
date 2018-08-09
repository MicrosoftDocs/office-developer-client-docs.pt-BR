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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cd70f5ee7b58bdf0b1fd61b1056bfc77e3e35992
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767614"
---
# <a name="iprofadmincopyprofile"></a>IProfAdmin::CopyProfile

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Um ponteiro para o nome do perfil para copiar.
    
 _lpszOldPassword_
  
> [in] Um ponteiro para a senha do perfil para copiar.
    
 _lpszNewProfileName_
  
> [in] Um ponteiro para o novo nome do perfil copiado.
    
 _ulUIParam_
  
> [in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o perfil é copiado. Sinalizadores a seguir podem ser definidos:
    
MAPI_DIALOG 
  
> Exibe uma caixa de diálogo que solicita ao usuário a senha correta do perfil para copiar. Se esse sinalizador não estiver definida, nenhuma caixa de diálogo é exibida.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O perfil foi copiado com êxito.
    
MAPI_E_ACCESS_DENIED 
  
> O nome do novo perfil é igual de um perfil existente.
    
MAPI_E_LOGON_FAILED 
  
> A senha para o perfil copiar estiver incorreta, e uma caixa de diálogo não pôde ser exibida para o usuário para solicitar a senha correta porque MAPI_DIALOG não foi definido no parâmetro _ulFlags_ . 
    
E_NOT_FOUND 
  
> O perfil especificado não existe.
    
MAPI_E_USER_CANCEL 
  
> O usuário cancelou a operação, geralmente clicando no botão **Cancelar** em uma caixa de diálogo. 
    
## <a name="remarks"></a>Comentários

O método **IProfAdmin::CopyProfile** faz uma cópia do perfil apontado pela _lpszOldProfileName_, dando a ele o nome apontada pela _lpszNewProfileName_. Copiar um perfil deixa a cópia com a mesma senha que o original.
  
O nome do perfil original, sua senha e a cópia pode ter até 64 caracteres de comprimento e pode incluir os seguintes caracteres:
  
- Todos os caracteres alfanuméricos, incluindo o caractere de sublinhado e ênfase.
    
- Espaços incorporados, mas não espaços à esquerda ou à direita.
    
Senhas de perfil não são suportadas em todos os sistemas operacionais. Nos sistemas operacionais que não oferecem suporte a senhas de perfil, _lpszOldPassword_ pode ser NULL ou um ponteiro para uma cadeia de caracteres de comprimento zero. 
  
Se _lpszOldPassword_ for definido como NULL, o perfil a ser copiado exige uma senha e o sinalizador MAPI_DIALOG está definido; uma caixa de diálogo que solicita ao usuário para fornecer a senha é exibida. Se uma senha é exigida, mas _lpszOldPassword_ for definido como nulo e o sinalizador MAPI_DIALOG não estiver definido, **CopyProfile** retorna MAPI_E_LOGON_FAILED. 
  
## <a name="see-also"></a>Confira também



[IProfAdmin : IUnknown](iprofadminiunknown.md)

