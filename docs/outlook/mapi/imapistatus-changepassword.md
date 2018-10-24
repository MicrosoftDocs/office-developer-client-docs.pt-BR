---
title: IMAPIStatusChangePassword
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIStatus.ChangePassword
api_type:
- COM
ms.assetid: 0cd1026a-342d-4d05-91ed-d3decced5bf3
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e09a1de5f85edd7e352a090c573fed9ca16f017f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565547"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Modifica a senha de um provedor de serviços sem exibir uma interface do usuário. Opcionalmente, esse método é suportado nos objetos de status que implementam provedores de serviços.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpOldPass_
  
> [in] Um ponteiro para a senha antiga.
    
 _lpNewPass_
  
> [in] Um ponteiro para a nova senha.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o formato das senhas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As senhas são no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as senhas são no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A modificação de senha foi bem-sucedida.
    
MAPI_E_NO_ACCESS 
  
> A senha antiga apontada pela _lpOldPass_ é inválida. 
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não suporta essa operação, conforme indicado pela ausência do sinalizador STATUS_CHANGE_PASSWORD na propriedade de **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.
    
## <a name="remarks"></a>Comentários

Nem todos os objetos de status suportam ao método **IMAPIStatus:: ChangePassword** . Ele é suportado somente por provedores de serviços que exigem que os clientes a digitar uma senha. Nenhum dos objetos status que implementa MAPI suporte à operação de alteração de senha. 
  
 **ChangePassword** modifica uma senha programaticamente, sem interação do usuário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Provedores de transporte remoto implementam **ChangePassword** conforme especificado aqui. Não há nenhuma considerações especiais. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônico de PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

