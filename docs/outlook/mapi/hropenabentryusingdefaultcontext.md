---
title: HrOpenABEntryUsingDefaultContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17cba69b-2b25-4b99-99d9-ec68fb8a35b5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f60c4d3761694439d10b073fda5bc36443c13e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434337"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa a mesma função que [HrOpenABEntryWithExchangeContext,](hropenabentrywithexchangecontext.md) exceto que ele usa **o emsmdbUID** herdável como o parâmetro _pEmsmdbUID._ Não use essa função, a menos que você não possa obter o **emsmdbUID** correto para a chamada para [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrOpenABEntryUsingDefaultContext(
  LPMAPISESSION pmsess,
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

 _pmsess_
  
> [in] O **IMAPISession conectado.** Não pode ser NULL.
    
 _pAddrBook_
  
> [in] O livro de endereços usado para abrir o identificador de entrada. Não pode ser NULL.
    
 _cbEntryID_
  
> [in] A contagem de byte do identificador de entrada especificado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
>  [in] Um ponteiro para o identificador de entrada que representa a entrada do livro de endereços a ser aberta. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) da interface que é usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão [é IMailUser : IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList : IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir  _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a entrada é aberta. Os sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS
  
> Solicita que a entrada seja aberta com as permissões máximas de rede e cliente permitidas. Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor do address book tentará abrir a entrada com permissão de leitura e gravação. O cliente pode recuperar o nível de acesso concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usa apenas o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que a chamada seja bem-sucedida, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Usa somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.
    
MAPI_MODIFY
  
> Solicita que a entrada seja aberta com permissão de leitura e gravação. Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que a permissão de leitura e gravação foi concedida independentemente de MAPI_MODIFY está definida.
    
MAPI_NO_CACHE
  
> Não usa o livro de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de agenda do Exchange.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    

