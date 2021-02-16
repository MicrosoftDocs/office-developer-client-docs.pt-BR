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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436430"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara duas **entryIDs** do livro de endereços com segurança em um perfil do Exchange múltiplo. Esta função é uma função de substituição para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
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
  
> [in] O **IMAPISession conectado.** Não pode ser NULL.
    
 _pEmsmdbUID_
  
> [in] Um ponteiro para **um emsmdbUID** que identifica o Serviço do Exchange que contém o Exchange Address Book Provider que essa função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não for um identificador de entrada do Exchange Address Book Provider, esse parâmetro será ignorado e a chamada de função se comportará como [IAddrBook::D etails](iaddrbook-details.md). Se esse parâmetro for NULL ou zero MAPIUID, essa função se comportará como [IAddrBook::D etails](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] O livro de endereços usado para abrir o identificador de entrada. Não pode ser NULL.
    
 _cbEntryID1_
  
> [in] A contagem de byte do primeiro identificador de entrada especificado pelo parâmetro _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada que representa a entrada do livro de endereços a ser comparada.
    
 _cbEntryID2_
  
> [in] A contagem de byte do segundo identificador de entrada especificado pelo parâmetro _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada usado na comparação que representa a entrada do livro de endereços a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o local que contém os resultados da comparação. 
    

