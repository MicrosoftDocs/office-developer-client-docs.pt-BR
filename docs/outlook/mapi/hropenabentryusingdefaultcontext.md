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
ms.openlocfilehash: 879ba4afe85e1f6db31bd829411689b2dad58ed9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565463"
---
# <a name="hropenabentryusingdefaultcontext"></a>HrOpenABEntryUsingDefaultContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Realiza a mesma função que [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md) , exceto que ele usa o herdado **emsmdbUID** como o parâmetro _pEmsmdbUID_ . Não use essa função, a menos que você não pode obter o **emsmdbUID** correto para a chamada para [HrOpenABEntryWithExchangeContext](hropenabentrywithexchangecontext.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] O conectado **IMAPISession**. Ele não pode ser NULL.
    
 _pAddrBook_
  
> [in] O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser NULL.
    
 _cbEntryID_
  
> [in] A contagem de bytes do identificador de entrada especificada pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  [in] Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços para abrir. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) da interface do que é usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, ela é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêineres é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ para a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a entrada é aberta. Sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS
  
> Solicita que a entrada seja aberto com as permissões de rede e cliente máxima permitidas. Por exemplo, se o cliente tem de leitura e permissão de gravação, o provedor de catálogo de endereços tenta abrir a entrada com a leitura e a permissão de gravação. O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::GetProps](imapiprop-getprops.md) da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Usa apenas o catálogo de endereços offline para realizar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que a chamada tiver êxito, potencialmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes à entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Usa apenas a GAL para realizar a resolução de nomes. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_MODIFY
  
> Solicitações que a entrada ser aberto com leia e permissão de gravação. Porque entradas são abertas com acesso somente leitura por padrão, os clientes não devem presumir que ler e gravar a permissão foi concedida independentemente MAPI_MODIFY é definida.
    
MAPI_NO_CACHE
  
> Não usa o catálogo de endereços offline para executar a resolução de nome. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo da entrada aberta.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro da entrada aberta.
    

