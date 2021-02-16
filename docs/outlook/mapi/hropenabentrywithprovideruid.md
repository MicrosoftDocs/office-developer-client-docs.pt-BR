---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 20344185ffcbd90017fa3c3493218bd9b3ddfd74
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408891"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre a **entryID** usando o Address Book do Exchange identificado por  _pEmsabpUID_. Esta função funciona de forma semelhante a [IAddrBook::OpenEntry,](iaddrbook-openentry.md) exceto pelo fato de que o uso dessa função garante que [IAddrBook::OpenEntry](iaddrbook-openentry.md) seja aberto usando o provedor do Exchange Address Book esperado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrOpenABEntryWithProviderUID(
  const MAPIUID *pEmsabpUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parâmetros

 _pEmsmdbUID_
  
> [in] Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o Exchange Address Book Provider que essa função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do Exchange Address Book Provider, esse parâmetro será ignorado e a chamada de função se comportará como [IAddrBook::D etails](iaddrbook-details.md). Se esse parâmetro for NULL ou zero MAPIUID, essa função se comportará como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] O livro de endereços usado para abrir o identificador de entrada. Não pode ser NULL.
    
 _cbEntryID_
  
> [in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) da interface que é usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
 _ulFlags_
  
> [in] Uma bitmask de sinalizadores que controla como a entrada é aberta, os sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS
  
> Solicita que a entrada seja aberta com as permissões máximas de rede e cliente permitidas. Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor do address book tentará abrir a entrada com permissão de leitura e gravação. O cliente pode recuperar o nível de acesso concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Use somente o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que a chamada seja bem-sucedida, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Use somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
MAPI_MODIFY
  
> Solicita que a entrada seja aberta com permissão de leitura e gravação. Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura e gravação foi concedida independentemente de MAPI_MODIFY está definida.
    
MAPI_NO_CACHE
  
> Não use o livro de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    

