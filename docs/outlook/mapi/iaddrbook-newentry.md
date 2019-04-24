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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 285da82d143524d2b2cf73ed3e5f1e3aeef6f9b3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336712"
---
# <a name="iaddrbooknewentry"></a>IAddrBook::NewEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um novo destinatário a um contêiner de catálogo de endereços ou à lista de destinatários de uma mensagem de saída.
  
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
  
> no Uma alça para a janela pai da caixa de diálogo.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o tipo de texto que é usado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> As cadeias de caracteres passadas estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 _cbEIDContainer_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> no Um ponteiro para o identificador de entrada do contêiner onde o novo destinatário deve ser adicionado. Se o parâmetro _cbEIDContainer_ for zero, o método **NewEntry** retornará um identificador de entrada de destinatário e uma lista de modelos como se o método [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) fosse chamado. 
    
 _cbEIDNewEntryTpl_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> no Um ponteiro para um modelo one-off que será usado para criar o novo destinatário. Se _cbEIDNewEntryTpl_ for zero e _lpEIDNewEntryTpl_ for nulo, **NewEntry** exibirá uma caixa de diálogo com a qual o usuário pode selecionar a partir de uma lista de modelos para adicionar novas entradas. 
    
 _lpcbEIDNewEntry_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> bota Um ponteiro para um ponteiro para o novo identificador de entrada do destinatário.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova entrada do catálogo de endereços foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **NewEntry** cria uma nova entrada de catálogo de endereços, a ser adicionada diretamente a um contêiner ou usada para endereçar uma mensagem de saída. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você deseja que a nova entrada seja adicionada a um contêiner específico, defina _lpEIDContainer_ para o identificador de entrada do contêiner e _cbEIDContainer_ para a contagem de bytes no identificador de entrada. 
  
Se quiser que a nova entrada seja adicionada à lista de destinatários de uma mensagem de saída, defina _lpEIDContainer_ como nulo e _cbEIDContainer_ como zero. 
  
Se você deseja permitir que o usuário de um aplicativo cliente selecione o tipo de entrada a ser criado, passe zero em _cbEIDNewEntryTpl_ e nulo no _lpEIDNewEntryTpl_. O método **NewEntry** exibe a tabela de one-off MAPI, uma lista de modelos suportados pelo MAPI e por cada provedor de catálogo de endereços na sessão. Cada modelo pode criar uma entrada de destinatário para um ou mais tipos de endereço. 
  
Se você quiser manter o identificador de entrada da nova entrada, passe os ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry_ . Você é responsável por liberar esse identificador de entrada quando terminar de fazê-lo chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar um modelo específico para adicionar uma nova entrada a um contêiner modificável, use o procedimento a seguir:
  
1. Chame o método [IMAPISession:: OpenEntry](imapisession-openentry.md) para abrir o contêiner de destino e defina o parâmetro _lpEntryID_ para o identificador de entrada do contêiner. 
    
2. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner de destino e defina o _parâmetro ulPropTag_ como **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro _lpiid_ para IID_IMAPITable. O contêiner retornará uma tabela única que lista todos os modelos compatíveis com a criação de novas entradas. 
    
3. Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar. A coluna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço que tem suporte no modelo.
    
4. Chame o método **NewEntry** e defina _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado. O identificador de entrada será a coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo na tabela one-off. Passe zero em _cbEIDContainer_ e nulo no _lpEIDContainer_. Passe um ponteiro válido no parâmetro _lppEIDNewEntry_ se você quiser manter o identificador de entrada da nova entrada. 
    
## <a name="see-also"></a>Confira também



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)

