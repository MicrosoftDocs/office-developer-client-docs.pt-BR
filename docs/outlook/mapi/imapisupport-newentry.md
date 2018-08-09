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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ae2a19d556fc9819312ce822f9347edcd6edc0d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767253"
---
# <a name="imapisupportnewentry"></a>IMAPISupport::NewEntry

  
  
**Aplica-se a**: Outlook 
  
Adiciona um novo destinatário diretamente para um contêiner de catálogo de endereços ou a lista de destinatários de uma mensagem de saída.
  
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
  
> [in] Uma alça para a janela pai da caixa de diálogo.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _cbEIDContainer_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDContainer_ . 
    
 _lpEIDContainer_
  
> [in] Um ponteiro para o identificador de entrada do contêiner para receber a nova entrada. Se _cbEIDContainer_ for 0 e _lpEIDContainer_ é NULL, **NewEntry** cria um identificador de entrada únicos que é do mesmo tipo, conforme é gerado por uma chamada ao método [IMAPISupport::CreateOneOff](imapisupport-createoneoff.md) . 
    
 _cbEIDNewEntryTpl_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEIDNewEntryTpl_ . 
    
 _lpEIDNewEntryTpl_
  
> [in] Um ponteiro para o identificador de entrada do modelo a ser usado para criar a nova entrada. Se _cbEIDNewEntryTpl_ for 0 e _lpEIDNewEntryTpl_ é NULL, **NewEntry** exibe uma caixa de diálogo que permite ao usuário selecionar de uma lista de modelos para adicionar novas entradas. 
    
 _lpcbEIDNewEntry_
  
> [out] Um ponteiro para a contagem de bytes no identificador de entrada apontado pelo parâmetro _lppEIDNewEntry_ . 
    
 _lppEIDNewEntry_
  
> [out] Um ponteiro para um ponteiro para o identificador de entrada da entrada recém-criado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A nova entrada foi criada com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::NewEntry** é implementado para objetos de suporte do provedor de catálogo de endereços. Provedores de catálogo de endereço chamarem **NewEntry** para criar uma nova entrada Catálogo de endereços a ser adicionado diretamente em um contêiner ou a ser usado para resolver uma mensagem de saída. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se desejar que a nova entrada a ser adicionado a um contêiner específico, defina _lpEIDContainer_ como identificador de entrada e a _cbEIDContainer_ para a contagem de bytes no identificador de entrada do contêiner. 
  
Se desejar que a nova entrada a ser adicionado à lista de destinatários de uma mensagem de saída, defina _lpEIDContainer_ como nulo e _cbEIDContainer_ como 0. 
  
Se você quiser permitir que o usuário de um aplicativo cliente para selecionar o tipo de entrada a ser criado, passe 0 _cbEIDNewEntryTpl_ e NULL no _lpEIDNewEntryTpl_. **NewEntry** exibe a tabela único MAPI, uma lista de modelos que oferecem suporte a MAPI e cada um dos provedores de catálogo de endereços na sessão. Cada modelo pode criar uma entrada para um ou mais tipos de endereço do destinatário. 
  
Se você deseja manter o identificador de entrada da nova entrada, passe ponteiros válidos nos parâmetros _lpcbEIDNewEntry_ e _lppEIDNewEntry_ . Você é responsável por liberar esse identificador de entrada quando terminar com ele chamando a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
Para usar um modelo específico para adicionar uma nova entrada de um contêiner modificável, use o procedimento a seguir:
  
1. Chame o método [IMAPISupport::OpenEntry](imapisupport-openentry.md) para abrir o contêiner de destino e defina o parâmetro _lpEntryID_ para o identificador de entrada do contêiner. 
    
2. Chamar o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner de destino e defina o parâmetro _ulPropTag_ para **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) e o parâmetro _lpiid_ como IID_IMAPITable. O contêiner retornará uma tabela único que lista todos os modelos ao qual ele oferece suporte para a criação de novas entradas. 
    
3. Recupere a linha que representa o modelo para o tipo específico de entrada que você deseja criar. A coluna de **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) indica o tipo de endereço que é suportado pelo modelo. 
    
4. Chamar **IMAPISupport::NewEntry** e defina o parâmetro _lpEIDNewEntryTpl_ para o identificador de entrada do modelo selecionado. O identificador de entrada é a coluna **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) da linha do modelo da tabela único. Passe 0 _cbEIDContainer_ e NULL no _lpEIDContainer_. Passe um ponteiro válido no parâmetro _lppEIDNewEntry_ se você deseja manter o identificador de entrada da nova entrada. 
    
## <a name="see-also"></a>Confira também



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport::OpenEntry](imapisupport-openentry.md)
  
[Propriedade canônica PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

