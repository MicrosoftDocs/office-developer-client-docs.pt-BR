---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 5db1b45f42365837d7b0e7af91f859f221ff687b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766788"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Aplica-se a**: Outlook 
  
Retorna o identificador de entrada do catálogo de endereços global para o serviço Exchange identificado pela _pEmsmdbUID_. O identificador de entrada retornados deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Par�metros

 _pSess_
  
> [in] O conectado IMAPISession. Ele não pode ser NULL.
    
 _pAddrBook_
  
> [in] O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser NULL.
    
 _pEmsmdbUID_
  
> [in] Um ponteiro para uma **emsmdbUID** que identifica a GAL do serviço Exchange a ser recuperado. Se _pEmsmdbUID_ for NULL ou o UID zero, essa função obtém a GAL herdada do serviço do Exchange. 
    
 _lpcbeid_
  
> [out] Um ponteiro para a contagem de bytes do identificador de entrada da lista de endereços global.
    
 _lppeid_
  
> [out] Um ponteiro para o identificador de entrada da lista de endereços global. Isso deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).
    

