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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419986"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Faz alterações em uma seção de perfil de armazenamento de mensagens permanente.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que indica o tipo de armazenamento de mensagens. O sinalizador a seguir pode ser definido:
    
MDB_TEMPORARY 
  
> O armazenamento de mensagens é temporário e não deve ser adicionado à tabela do armazenamento de mensagens. Quando MDB_TEMPORARY é definido, **ModifyProfile** retorna S_OK imediatamente. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As alterações feitas na seção de perfil foram bem-sucedidas.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::ModifyProfile** é implementado para objetos de suporte do provedor de armazenamento de mensagens. Os provedores de armazenamento de mensagens **chamam ModifyProfile** para solicitar que o MAPI modifique suas informações de perfil. 
  
 **ModifyProfile adiciona** a seção de perfil associada ao provedor de chamada à lista de recursos instalados do provedor de armazenamento de mensagens. Isso faz com que o armazenamento de mensagens seja listado na tabela do armazenamento de mensagens, que está disponível para clientes por meio do método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) e ser aberto sem a exibição de uma caixa de diálogo. 
  
Se o MDB_TEMPORARY de dados estiver definido, MAPI não faz nada e o método retorna imediatamente com S_OK.
  
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

