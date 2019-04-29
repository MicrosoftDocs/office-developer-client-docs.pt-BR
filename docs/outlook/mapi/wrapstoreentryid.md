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
  
Converte um identificador de entrada interna do repositório de mensagens em um identificador de entrada mais utilizável pelo sistema de mensagens. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
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
  
> no Bitmask de sinalizadores. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI. 
    
 _szDLLName_
  
> no O nome da DLL do provedor de repositório de mensagens. 
    
 _cbOrigEntry_
  
> no Tamanho, em bytes, do identificador de entrada original para o repositório de mensagens. 
    
 _lpOrigEntry_
  
> no Ponteiro para uma [](entryid.md) estrutura ENTRYID que contém o identificador de entrada original. 
    
 _lpcbWrappedEntry_
  
> bota Ponteiro para o tamanho, em bytes, do novo identificador de entrada. 
    
 _lppWrappedEntry_
  
> bota Ponteiro para um ponteiro para uma **** estrutura ENTRYID que contém o novo identificador de entrada. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

Um objeto do repositório de mensagens mantém um identificador de entrada interno que é significativo apenas para os provedores de serviços coresidentes com o repositório de mensagens. Para outros componentes de mensagens, o MAPI fornece uma versão encapsulada do identificador de entrada interna que o torna reconhecível como pertencente ao repositório de mensagens. Os provedores de serviço de coresidente devem sempre receber o identificador de entrada de repositório de mensagens não wrapped original; os aplicativos cliente devem sempre ter a versão empacotada, que pode ser usada em qualquer lugar no domínio de mensagens e em outros domínios. 
  
Um provedor de serviços pode encapsular um identificador de entrada de repositório de mensagens usando a função **WrapStoreEntryID** ou o método [IMAPISupport:: WrapStoreEntryID](imapisupport-wrapstoreentryid.md) , que chama a função **WrapStoreEntryID** . O provedor deve encapsular o identificador de entrada ao expor a propriedade **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) do repositório de mensagens ou gravá-lo em uma seção de perfil e ao expor o **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)) Propriedades. O MAPI divide um identificador de entrada de repositório de mensagens ao responder a uma chamada a [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) . 
  
Quando um aplicativo cliente passa um identificador de entrada de repositório de mensagens quebrado para MAPI, por exemplo, em uma chamada a [IMAPISession:: OpenEntry](imapisession-openentry.md) , o MAPI desenvolve o identificador de entrada antes de usá-lo para chamar um método de provedor como [IMSProvider:: logon](imsprovider-logon.md) ou [ IMSProvider:: CompareStoreIDs](imsprovider-comparestoreids.md). 
  

