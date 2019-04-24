---
title: IMAPISupportModifyProfile
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.ModifyProfile
api_type:
- COM
ms.assetid: 33bef4ea-d6c0-4455-b95d-4b29edb9c0bc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4c296b12d2dc98c4ff8d94349298e9dda0fb9409
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316593"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz alterações em uma seção de perfil do repositório de mensagens permanente.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica o tipo de repositório de mensagens. O seguinte sinalizador pode ser definido:
    
MDB_TEMPORARY 
  
> O repositório de mensagens é temporário e não deve ser adicionado à tabela do repositório de mensagens. Quando MDB_TEMPORARY é definido, **ModifyProfile** retorna S_OK imediatamente. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As alterações na seção de perfil foram bem-sucedidas.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: ModifyProfile** é implementado para objetos de suporte do provedor de repositório de mensagens. Os provedores de repositório de mensagens chamam o **ModifyProfile** para solicitar que o MAPI modifique suas informações de perfil. 
  
 **ModifyProfile** adiciona a seção de perfil associada ao provedor de chamadas à lista de recursos do provedor de repositório de mensagens instalado. Isso faz com que o repositório de mensagens seja listado na tabela do repositório de mensagens, que está disponível para clientes por meio do método [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) , e a ser aberto sem a exibição de uma caixa de diálogo. 
  
Se o sinalizador MDB_TEMPORARY for definido, MAPI não fará nada e o método retornará imediatamente com S_OK.
  
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

