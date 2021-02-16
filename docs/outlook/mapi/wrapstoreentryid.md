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
ms.openlocfilehash: e797a80cf8659baa7ca935f94b3ab65c200530a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409206"
---
# <a name="wrapstoreentryid"></a>WrapStoreEntryID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte o identificador de entrada interno de um armazenamento de mensagens em um identificador de entrada mais usável pelo sistema de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
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
  
> [in] Máscara de bits de sinalizadores. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres estão no formato Unicode. Se o MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI. 
    
 _szDLLName_
  
> [in] O nome do provedor de armazenamento de mensagens DLL. 
    
 _cbOrigEntry_
  
> [in] Tamanho, em bytes, do identificador de entrada original para o armazenamento de mensagens. 
    
 _lpOrigEntry_
  
> [in] Ponteiro para uma [estrutura ENTRYID](entryid.md) que contém o identificador de entrada original. 
    
 _lpcbWrappedEntry_
  
> [out] Ponteiro para o tamanho, em bytes, do novo identificador de entrada. 
    
 _lppWrappedEntry_
  
> [out] Ponteiro para um ponteiro para uma **estrutura ENTRYID** que contém o novo identificador de entrada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um objeto de armazenamento de mensagens mantém um identificador de entrada interno que é significativo apenas para os provedores de serviços que se identificam com esse armazenamento de mensagens. Para outros componentes de mensagens, o MAPI fornece uma versão empacotada do identificador de entrada interna que o torna reconhecível, pois pertence ao armazenamento de mensagens. Os provedores de serviços Coresident sempre devem receber o identificador de entrada do armazenamento de mensagens original não mapeado; os aplicativos cliente sempre devem receber a versão empacotada, que pode ser usada em qualquer lugar no domínio de mensagens e em outros domínios. 
  
Um provedor de serviços pode quebrar um identificador de entrada do repositório de mensagens usando a função **WrapStoreEntryID** ou o método [IMAPISupport::WrapStoreEntryID,](imapisupport-wrapstoreentryid.md) que chama a **função WrapStoreEntryID.** O provedor deve quebrar o identificador de entrada ao expor a propriedade **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)do repositório de mensagens ou ao escrever em uma seção de perfil e ao expor a propriedade **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). MAPI wraps a message store entry identifier when responding to an [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) call. 
  
Quando um aplicativo cliente passa um identificador de entrada do repositório de mensagens empacotado para MAPI, por exemplo, em uma chamada [IMAPISession::OpenEntry,](imapisession-openentry.md) MAPI deswraps o identificador de entrada antes de usá-lo para chamar um método de provedor como [IMSProvider::Logon](imsprovider-logon.md) ou [IMSProvider::CompareStoreIDs](imsprovider-comparestoreids.md). 
  

