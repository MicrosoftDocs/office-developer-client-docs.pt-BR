---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a60ac0d7ab139f77aea87080e1ce37fee870e97b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437536"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Registra uma estrutura [MAPIUID](mapiuid.md) que representa exclusivamente o provedor de serviços. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Parâmetros

 _lpProviderID_
  
> [in] Um ponteiro para a estrutura **MAPIUID** que identifica o agendador de endereços ou o provedor de armazenamento de mensagens. 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A **estrutura MAPIUID** foi registrada com êxito. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::SetProviderUID** é implementado para objetos de suporte de provedor de armazenamento de endereços e de armazenamento de mensagens. Esses provedores chamam **SetProviderUID** para registrar um identificador exclusivo descrito na estrutura **MAPIUID** apontada por  _lpProviderID_. Os provedores incluem esse identificador em todos os identificadores de entrada que eles criam. 
  
MAPI uses the **MAPIUID** structure when it sends outbound messages to the MAPI spooler and to determine the appropriate provider for handling client requests. Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI examina a parte **MAPIUID** do identificador de entrada, mapeia para o provedor que a passou para **SetProviderUID** e chama **OpenEntry** desse provedor. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SetProviderUID no** momento do logon para registrar sua **estrutura MAPIUID.** MAPI allows address book and message store providers to register multiple identifiers. Quando você faz várias chamadas para **SetProviderUID**, ela sempre adiciona a estrutura **MAPIUID** ao conjunto de estruturas **MAPIUID** do provedor, mesmo se **o MAPIUID** for uma duplicata. **SetProviderUID** não pode remover um **MAPIUID**. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

