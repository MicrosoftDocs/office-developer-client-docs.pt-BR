---
title: WrapStoreEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WrapStoreEntryID
api_type:
- HeaderDef
ms.assetid: b20107e3-5e23-4cde-9cd6-670c914ea70a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: aff46cca7a7d530b2eede1790176058e3b91abc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770721"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Aplica-se a**: Outlook 
  
Converte o identificador de entrada interna do repositório de uma mensagem para um identificador de entrada mais utilizável pelo sistema de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
WrapStoreEntryID(
  ULONG ulFlags,
  LPSTR szDLLName,
  ULONG cbOrigEntry,
  LPENTRYID lpOrigEntry,
  ULONG * lpcbWrappedEntry,
  LPENTRYID * lppWrappedEntry
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Bitmask dos sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _szDLLName_
  
> [in] O nome do provedor de armazenamento de mensagem DLL. 
    
 _cbOrigEntry_
  
> [in] Tamanho, em bytes, do identificador de entrada original para o armazenamento de mensagens. 
    
 _lpOrigEntry_
  
> [in] Ponteiro para uma estrutura [ENTRYID](entryid.md) que contém o identificador de entrada original. 
    
 _lpcbWrappedEntry_
  
> [out] Ponteiro para o tamanho, em bytes, de um novo identificador de entrada. 
    
 _lppWrappedEntry_
  
> [out] Ponteiro para um ponteiro para uma estrutura **ENTRYID** que contém o novo identificador de entrada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um objeto de repositório de mensagem mantém um identificador interno de entrada que é significativo apenas para coresident de provedores de serviço com esse armazenamento de mensagens. Para outros componentes de mensagens, MAPI fornece uma versão com quebra do identificador interno de entrada que torna reconhecível conforme que pertencem ao repositório de mensagem. Provedores de serviços de coresident devem sempre ser dada o identificador de entrada de repositório desfeita da mensagem original; aplicativos cliente devem sempre ser dada a versão com quebra, que é, em seguida, pode ser usada em qualquer lugar no domínio de mensagens e em outros domínios. 
  
Um provedor de serviços pode quebrar um identificador de entrada do repositório de mensagem usando a função **WrapStoreEntryID** ou o método [IMAPISupport::WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , que chama a função **WrapStoreEntryID** . O provedor deve quebrar o identificador de entrada ao expor **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do armazenamento de mensagens propriedade ou gravá-lo em uma seção de perfil e ao expor **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) propriedade. Um identificador de entrada do repositório de mensagem é disposto MAPI ao responder a uma chamada [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . 
  
Quando um aplicativo cliente passa um identificador de entrada do repositório de mensagem com quebra para MAPI, por exemplo em uma chamada de [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI ou não, o identificador de entrada para utilizá-lo para chamar um método de provedor, como [IMSProvider::Logon](imsprovider-logon.md) ou [ IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

