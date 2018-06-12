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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 98e6331d5a9e52d5ae73ed12d8c045bdf226c2c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767242"
---
# <a name="imapisupportmodifyprofile"></a>IMAPISupport::ModifyProfile

  
  
**Aplica-se a**: Outlook 
  
Faz com que alterações a uma mensagem armazenar seção perfil permanente.
  
```cpp
HRESULT ModifyProfile(
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Armazene em uma bitmask dos sinalizadores que indica o tipo de mensagem. O seguinte sinalizador pode ser definido:
    
MDB_TEMPORARY 
  
> O armazenamento de mensagens é temporário e não deve ser adicionado à tabela de repositório de mensagem. Quando MDB_TEMPORARY estiver definido, o **ModifyProfile** Retorna S_OK imediatamente. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As alterações para a seção de perfil foram bem-sucedidas.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::ModifyProfile** é implementado para objetos de suporte do provedor de repositório de mensagem. Mensagem de chamada de provedores de repositório **ModifyProfile** para solicitar o MAPI para modificar suas informações de perfil. 
  
 **ModifyProfile** adiciona a seção de perfil que está associada com o provedor de chamada à lista de recursos do provedor de repositório de mensagem instalado. Isso faz com que o armazenamento de mensagens a serem listados na tabela de repositório de mensagens, que está disponível aos clientes através do método [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) e para ser aberto sem a exibição de uma caixa de diálogo. 
  
Se o sinalizador MDB_TEMPORARY estiver definido, MAPI não faz nada e o método retornará imediatamente com S_OK.
  
## <a name="see-also"></a>Confira também



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

