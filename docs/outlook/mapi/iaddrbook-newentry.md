---
title: IAddrBookNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.NewEntry
api_type:
- COM
ms.assetid: 8d2d786b-e621-456d-b087-3373df6f8ac5
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eaf472a380acd62cddb2c20c35335ccb1e2ce07f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585854"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um novo destinatário para um contêiner de catálogo de endereços ou a lista de destinatários de uma mensagem de saída.
  
```cpp
HRESULT NewEntry(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG cbEIDContainer,
  LPENTRYID lpEIDContainer,
  ULONG cbEIDNewEntryTpl,
  LPENTRYID lpEIDNewEntryTpl,
  ULONG FAR * lpcbEIDNewEntry,
  LPENTRYID FAR * lppEIDNewEntry
);
```

## <a name="parameters"></a>Parâmetros

 _ulUIParam_
  
> [in] Uma alça para a janela pai para a caixa de diálogo.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o tipo de texto que é usado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passada na estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 _cbEIDContainer_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Um ponteiro para o identificador de entrada do contêiner onde o novo destinatário deve ser adicionado. Se o parâmetro _cbEIDContainer_ for zero, o método **NewEntry** retorna um identificador de entrada do destinatário e uma lista de modelos como se o método [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) foi chamado. 
    
 _cbEIDNewEntryTpl_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Um ponteiro para um modelo único que será usado para criar o novo destinatário. Se _cbEIDNewEntryTpl_ for zero e _lpEIDNewEntryTpl_ é NULL, **NewEntry** exibe uma caixa de diálogo com a qual o usuário pode selecionar de uma lista de modelos para adicionar novas entradas. 
    
 _lpcbEIDNewEntry_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada do novo destinatário.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A nova entrada de catálogo de endereços foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **NewEntry** cria uma nova entrada de catálogo de endereços, a ser adicionado diretamente em um contêiner ou a ser usado para resolver uma mensagem de saída. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se desejar que a nova entrada a ser adicionado a um contêiner específico, defina _lpEIDContainer_ como identificador de entrada e a _cbEIDContainer_ para a contagem de bytes no identificador de entrada do contêiner. 
  
Se desejar que a nova entrada a ser adicionado à lista de destinatários de uma mensagem de saída, defina _lpEIDContainer_ como nulo e _cbEIDContainer_ como zero. 
  
Se você quiser permitir que o usuário de um aplicativo cliente para selecionar o tipo de entrada a ser criado, passe zero em _cbEIDNewEntryTpl_ e NULL no _lpEIDNewEntryTpl_. O método **NewEntry** exibe a tabela único MAPI, uma lista de modelos com suporte por MAPI e por cada provedor de catálogo de endereços na sessão. Cada modelo pode criar uma entrada para um ou mais tipos de endereço do destinatário. 
  
Se você deseja manter o identificador de entrada da nova entrada, passe ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry_ . Você é responsável por liberar esse identificador de entrada quando terminar com ele chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar um modelo específico para adicionar uma nova entrada de um contêiner modificável, use o procedimento a seguir:
  
1. Chame o método [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o contêiner de destino e defina o parâmetro _lpEntryID_ para o identificador de entrada do contêiner. 
    
2. Chamar o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner de destino e defina o parâmetro _ulPropTag_ para **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro _lpiid_ como IID_IMAPITable. O contêiner retornará uma tabela único que lista todos os modelos de qual ele oferece suporte para a criação de novas entradas. 
    
3. Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar. A coluna de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço que é suportado pelo modelo.
    
4. Chame o método **NewEntry** e defina _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado. O identificador de entrada terá a coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo da tabela único. Passe zero em _cbEIDContainer_ e NULL no _lpEIDContainer_. Passe um ponteiro válido no parâmetro _lppEIDNewEntry_ se você deseja manter o identificador de entrada da nova entrada. 
    
## <a name="see-also"></a>Confira também



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

