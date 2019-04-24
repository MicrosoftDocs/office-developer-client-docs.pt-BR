---
title: HrGetGALFromEmsmdbUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9b824e70-ed9a-490c-b777-8902a793fece
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b9a31fec93ec7fafc4d1565d63e4bc427ba4050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347828"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada do catálogo de endereços global para o serviço do Exchange identificado por _pEmsmdbUID_. O identificador de entrada retornado deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
HRESULT HrGetGALFromEmsmdbUID(
  LPMAPISESSION pSess,
  LPADRBOOK lpAdrBook,
  const MAPIUID * pEmsmdbUID,
  ULONG * lpcbeid,
  LPENTRYID * lppeid
);
```

## <a name="parameters"></a>Parâmetros

 _pSess_
  
> no O IMAPISession conectado. Ele não pode ser nulo.
    
 _pAddrBook_
  
> no O catálogo de endereços usado para abrir o identificador de entrada. Ele não pode ser nulo.
    
 _pEmsmdbUID_
  
> no Um ponteiro para um **emsmdbUID** que identifica a GAL do serviço do Exchange a ser recuperado. Se _pEmsmdbUID_ for nulo ou a UID zero, essa função obterá a GAL herdada do serviço do Exchange. 
    
 _lpcbeid_
  
> bota Um ponteiro para o número de bytes do identificador de entrada da lista de endereços global.
    
 _lppeid_
  
> bota Um ponteiro para o identificador de entrada da lista de endereços global. Isso deve ser liberado usando o [MAPIFreeBuffer](mapifreebuffer.md).
    

