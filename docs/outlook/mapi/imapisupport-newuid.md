---
title: IMAPISupportNewUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewUID
api_type:
- COM
ms.assetid: 7994477d-5207-4335-b538-69c98782d52d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 14be41c21244abe8c54261a95a410828c973d66b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767255"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Aplica-se a**: Outlook 
  
Cria uma nova estrutura [MAPIUID](mapiuid.md) a ser usado como um identificador exclusivo. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parâmetros

 _lpMuid_
  
> Um ponteiro para a nova estrutura **MAPIUID** . 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A nova estrutura **MAPIUID** foi criada. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::NewUID** é implementado para todos os objetos de suporte. Provedores de serviço e serviços de mensagem chamada **NewUID** sempre que precisam gerar um identificador exclusivo de longo prazo. Uma mensagem armazenar provedor, por exemplo, talvez chamada **NewUID** para obter um **MAPIUID** para colocar na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de uma mensagem recém-criado.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não confunda a estrutura **MAPIUID** que você registre na hora do logon com as estruturas de **MAPIUID** que o método **NewUID** cria. A estrutura **MAPIUID** que você registre quando você chama o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa seu catálogo de endereços ou mensagem armazenar provedor para MAPI e é usado para distinguir os identificadores de entrada que criar provedores diferentes. Essa estrutura **MAPIUID** deve ser codificadas e não é obtida por meio de uma chamada para **NewUID**.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

