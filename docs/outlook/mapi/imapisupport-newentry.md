---
title: IMAPISupportNewEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.NewEntry
api_type:
- COM
ms.assetid: 588d002b-8412-4ab9-9757-04ad89e0a6f8
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3468e4a92787e440f230d60ab31f37526fe7d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405454"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona um novo destinatário diretamente a um contêiner de catálogo de endereços ou à lista de destinatários de uma mensagem de saída.
  
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
  
> no Serve deve ser zero.
    
 _cbEIDContainer_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> no Um ponteiro para o identificador de entrada do contêiner para receber a nova entrada. Se _cbEIDContainer_ for 0 e _lpEIDContainer_ for nulo, **NewEntry** criará um identificador de entrada one-off que é o mesmo tipo que é gerado por uma chamada para o método [IMAPISupport:: CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> no Um ponteiro para o identificador de entrada do modelo a ser usado para criar a nova entrada. Se _cbEIDNewEntryTpl_ for 0 e _lpEIDNewEntryTpl_ for nulo, **NewEntry** exibirá uma caixa de diálogo que permite ao usuário selecionar de uma lista de modelos para adicionar novas entradas. 
    
 _lpcbEIDNewEntry_
  
> bota Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> bota Um ponteiro para um ponteiro para o identificador de entrada da entrada recém-criada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A nova entrada foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: NewEntry** é implementado para objetos de suporte do provedor de catálogo de endereços. Os provedores de catálogo de endereços chamam o **NewEntry** para criar uma nova entrada de catálogo de endereços a ser adicionada diretamente a um contêiner ou para ser usada para endereçar uma mensagem de saída. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se você deseja que a nova entrada seja adicionada a um contêiner específico, defina _lpEIDContainer_ para o identificador de entrada do contêiner e _cbEIDContainer_ para a contagem de bytes no identificador de entrada. 
  
Se quiser que a nova entrada seja adicionada à lista de destinatários de uma mensagem de saída, defina _lpEIDContainer_ como nulo e _cbEIDContainer_ como 0. 
  
Se você deseja permitir que o usuário de um aplicativo cliente selecione o tipo de entrada a ser criada, passe 0 em _cbEIDNewEntryTpl_ e nulo no _lpEIDNewEntryTpl_. O **NewEntry** exibe a tabela de one-off MAPI, uma lista de modelos que o MAPI e cada um dos provedores de catálogo de endereços na sessão dão suporte. Cada modelo pode criar uma entrada de destinatário para um ou mais tipos de endereço. 
  
Se você quiser manter o identificador de entrada da nova entrada, passe os ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry_ . Você é responsável por liberar esse identificador de entrada quando terminar de fazê-lo chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar um modelo específico para adicionar uma nova entrada a um contêiner modificável, use o procedimento a seguir:
  
1. Chame o método [IMAPISupport:: OpenEntry](imapisupport-openentry.md) para abrir o contêiner de destino e defina o parâmetro _lpEntryID_ para o identificador de entrada do contêiner. 
    
2. Chame o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner de destino e defina o _parâmetro ulPropTag_ como **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro _lpiid_ para IID_IMAPITable. O contêiner retornará uma tabela única que lista todos os modelos compatíveis com a criação de novas entradas. 
    
3. Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar. A coluna **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço que tem suporte no modelo. 
    
4. Chame **IMAPISupport:: NewEntry** e defina o parâmetro _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado. O identificador de entrada é a coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo na tabela one-off. Passe 0 em _cbEIDContainer_ e nulo no _lpEIDContainer_. Passe um ponteiro válido no parâmetro _lppEIDNewEntry_ se você quiser manter o identificador de entrada da nova entrada. 
    
## <a name="see-also"></a>Confira também



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

