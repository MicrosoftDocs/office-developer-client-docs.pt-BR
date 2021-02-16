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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a38f7ea475f8a5cbad4f1cc295c3e2550ea8cd66
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406994"
---
# <a name="imapisupportnewuid"></a>IMAPISupport::NewUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Cria uma nova [estrutura MAPIUID](mapiuid.md) a ser usada como um identificador exclusivo. 
  
```cpp
HRESULT NewUID(
LPMAPIUID lpMuid
);
```

## <a name="parameters"></a>Parâmetros

 _lpMuid_
  
> Um ponteiro para a nova **estrutura MAPIUID.** 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova **estrutura MAPIUID** foi criada. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::NewUID** é implementado para todos os objetos de suporte. Provedores de serviços e serviços de mensagens chamam **NewUID** sempre que precisam gerar um identificador exclusivo de longo prazo. Um provedor de armazenamento de mensagens, por exemplo, pode chamar **NewUID** para obter um **MAPIUID** a ser colocado na propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) de uma mensagem recém-criada.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Não confunda a **estrutura MAPIUID** que você registra no momento do logon com as estruturas **MAPIUID** que o **método NewUID** cria. A estrutura **MAPIUID** que você registra ao chamar o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) representa seu livro de endereços ou provedor de armazenamento de mensagens para MAPI e é usada para distinguir identificadores de entrada que diferentes provedores criam. Essa **estrutura MAPIUID** deve ser codificada e não obtida por meio de uma chamada para **NewUID**.
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

