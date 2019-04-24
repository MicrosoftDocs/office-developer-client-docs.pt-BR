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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347814"
---
# <a name="hropenabentrywithprovideruid"></a>HrOpenABEntryWithProviderUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre a **EntryID** usando o catálogo de endereços do Exchange identificado pelo _pEmsabpUID_. Essa função funciona de forma semelhante a [IAddrBook:: OpenEntry](iaddrbook-openentry.md) exceto que usar essa função garante que o [IAddrBook:: OpenEntry](iaddrbook-openentry.md) seja aberto usando o provedor de catálogo de endereços do Exchange esperado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp. h  <br/> |
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
  
> no Um ponteiro para um **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que essa função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do provedor de catálogo de endereços do Exchange, este parâmetro será ignorado e a chamada de função se comformará como [IAddrBook::D etails](iaddrbook-details.md). Se esse parâmetro for nulo ou um MAPIUID zero, essa função se comformará como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> no O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser nulo.
    
 _cbEntryID_
  
> no A contagem de bytes do identificador de entrada especificado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
>  no Um ponteiro para o identificador de entrada que representa a entrada do catálogo de endereços a ser aberta. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) da interface que é usado para acessar a entrada aberta. Passar NULL retorna a interface padrão do objeto. Para usuários de mensagens, a interface padrão é [IMailUser: IMAPIProp](imailuserimapiprop.md). Para listas de distribuição, é [IDistList: IMAPIContainer](idistlistimapicontainer.md)e para contêiners, é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). Os chamadores podem definir _lpInterface_ como a interface padrão apropriada ou uma interface na hierarquia de herança. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controlam o modo como a entrada é aberta, os seguintes sinalizadores podem ser definidos:
    
MAPI_BEST_ACCESS
  
> Solicita que a entrada seja aberta com o máximo permitido de rede e permissões de cliente. Por exemplo, se o cliente tiver permissão de leitura e gravação, o provedor de catálogo de endereços tentará abrir a entrada com permissão de leitura e gravação. O cliente pode recuperar o nível de acesso que foi concedido chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps da entrada aberta e recuperando a propriedade PR_ACCESS_LEVEL (PidTagAccessLevel). 
    
MAPI_CACHE_ONLY
  
> Use apenas o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS
  
> Permite que a chamada seja bem-sucedida, possivelmente antes que a entrada seja totalmente aberta e disponível, indicando que as chamadas subsequentes para a entrada podem retornar um erro.
    
MAPI_GAL_ONLY
  
> Use somente a GAL para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_MODIFY
  
> Solicita que a entrada seja aberta com permissões de leitura e gravação. Como as entradas são abertas com acesso somente leitura por padrão, os clientes não devem supor que a permissão de leitura e gravação tenha sido concedida independentemente de o MAPI_MODIFY ser definido.
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo de entrada aberta.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro da entrada aberta.
    

