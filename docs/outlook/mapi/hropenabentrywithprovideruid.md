---
title: HrOpenABEntryWithProviderUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 83821a86-abff-460c-bb8e-9fd9d232dc6b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: e33e656e70802437ab8b8717c5e175e2a13e384e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766795"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Aplica-se a**: Outlook 
  
Abre a **entryID** usando o catálogo de endereços do Exchange identificado pela _pEmsabpUID_. Essa função funciona de maneira semelhante para [IAddrBook::OpenEntry](iaddrbook-openentry.md) , exceto que o uso da função garante que [IAddrBook::OpenEntry](iaddrbook-openentry.md) é aberto usando o provedor de catálogo de endereços do Exchange esperado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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

## <a name="parameters"></a>Par�metros

 _pEmsmdbUID_
  
> [in] Um ponteiro para uma **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não é um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função se comporta como [IAddrBook::Details](iaddrbook-details.md). Se esse parâmetro for NULL ou um zero MAPIUID, essa função se comporta como [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser NULL.
    
 _cbEntryID_
  
> [in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  [in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) da interface do que é usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, ele é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o como a entrada é aberta, sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS
  
> Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas. Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação. O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Use somente o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Use somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_MODIFY
  
> Solicitações que a entrada ser aberto com leia e permissão de gravação. Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nome. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo da entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    

