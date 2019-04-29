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
ms.openlocfilehash: 2c824b6b994bfb31b5e6ac7fed0eeae88c47cdba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410354"
---
# <a name="imapistatuschangepassword"></a>IMAPIStatus::ChangePassword

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Modifica a senha de um provedor de serviços sem exibir uma interface de usuário. Opcionalmente, este método é compatível com objetos de status que os provedores de serviços implementam.
  
```cpp
HRESULT ChangePassword(
  LPSTR lpOldPass,
  LPSTR lpNewPass,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpOldPass_
  
> no Um ponteiro para a senha antiga.
    
 _lpNewPass_
  
> no Um ponteiro para a nova senha.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o formato das senhas. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As senhas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as senhas estarão no formato ANSI.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A modificação de senha foi bem-sucedida.
    
MAPI_E_NO_ACCESS 
  
> A senha antiga indicada por _lpOldPass_ é inválida. 
    
MAPI_E_NO_SUPPORT 
  
> O objeto status não oferece suporte a essa operação, conforme indicado pela ausência do sinalizador STATUS_CHANGE_PASSWORD na propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) do objeto status.
    
## <a name="remarks"></a>Comentários

Nem todos os objetos de status dão suporte ao método **IMAPIStatus:: ChangePassword** . Só há suporte para os provedores de serviços que exigem que os clientes insiram uma senha. Nenhum dos objetos de status que o MAPI implementa oferece suporte à operação de alteração de senha. 
  
 **ChangePassword** modifica uma senha por meio de programação, sem interação do usuário. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Os provedores de transporte remotos implementam a **ChangePassword** conforme especificado aqui. Não há considerações especiais. 
  
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)
  
[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)

