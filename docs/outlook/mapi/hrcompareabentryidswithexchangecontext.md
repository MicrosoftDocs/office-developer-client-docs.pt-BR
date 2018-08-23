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
ms.openlocfilehash: eb91f4998f94ffafbc33b6024228945f7c91cf43
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564987"
---
# <a name="hrcompareabentryidswithexchangecontext"></a>HrCompareABEntryIDsWithExchangeContext

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois de catálogo de endereços **entryIDs** com segurança em um perfil do Exchange vários. Esta é uma função de substituição para [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> [in] O conectado **IMAPISession**. Ele não pode ser NULL.
    
 _pEmsmdbUID_
  
> [in] Um ponteiro para uma **emsmdbUID** que identifica o serviço do Exchange que contém o provedor de catálogo de endereços do Exchange que esta função deve usar para exibir detalhes sobre o identificador de entrada. Se o identificador de entrada de entrada não é um identificador de entrada do provedor de catálogo de endereços do Exchange, esse parâmetro será ignorado e a chamada de função se comporta como [IAddrBook::Details](iaddrbook-details.md). Se esse parâmetro for NULL ou um zero MAPIUID, essa função se comporta como [IAddrBook::Details](iaddrbook-details.md).
    
 _pAddrBook_
  
> [in] O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser NULL.
    
 _cbEntryID1_
  
> [in] A contagem de bytes do primeiro identificador de entrada especificada pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada que representa a entrada do catálogo de endereços para comparar.
    
 _cbEntryID2_
  
> [in] A contagem de bytes do identificador da segunda entrada especificado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada utilizado na comparação que representa a entrada do catálogo de endereços para comparar.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o local que contém os resultados da comparação. 
    

