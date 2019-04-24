---
title: HrCompareABEntryIDsWithExchangeContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e537c25f-51b5-4f06-a20a-44ee540b9a1f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4bada5913623e2eb463a9e72347bd31eb22c414b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348073"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois catálogos de endereços **entryIDs** com segurança em um perfil de vários Exchange. Esta função é uma função de substituição para [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrCompareABEntryIDsWithExchangeContext(
  LPMAPISESSION pmsess,
  const MAPIUID *pEmsmdbUID,
  LPADRBOOK pAddrBook,
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG * lpulResult
);
```

## <a name="parameters"></a>Parâmetros

 _pmsess_
  
> no O **IMAPISession**conectado. Ele não pode ser nulo.
    
 _pEmsmdbUID_
  
> no Um ponteiro para um **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que essa função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do provedor de catálogo de endereços do Exchange, este parâmetro será ignorado e a chamada de função se comformará como [IAddrBook::D etails](iaddrbook-details.md). Se esse parâmetro for nulo ou um MAPIUID zero, essa função se comformará como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> no O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser nulo.
    
 _cbEntryID1_
  
> no A contagem de bytes do primeiro identificador de entrada especificado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> no Um ponteiro para o primeiro identificador de entrada que representa a entrada do catálogo de endereços a ser comparada.
    
 _cbEntryID2_
  
> no A contagem de bytes do segundo identificador de entrada especificado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> no Um ponteiro para o segundo identificador de entrada usado na comparação que representa a entrada do catálogo de endereços a ser comparada.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulResult_
  
> bota Um ponteiro para o local que contém os resultados da comparação. 
    

