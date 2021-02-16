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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439104"
---
# <a name="hrgetgalfromemsmdbuid"></a>HrGetGALFromEmsmdbUID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Retorna o identificador de entrada do livro de endereços global para o serviço exchange identificado por  _pEmsmdbUID_. O identificador de entrada retornado deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |abhelp.h  <br/> |
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
  
> [in] O IMAPISession conectado. Não pode ser NULL.
    
 _pAddrBook_
  
> [in] O livro de endereços usado para abrir o identificador de entrada. Não pode ser NULL.
    
 _pEmsmdbUID_
  
> [in] Um ponteiro para **um emsmdbUID** que identifica a GAL do Serviço do Exchange a ser recuperada. Se  _pEmsmdbUID_ for NULL ou o UID zero, essa função obtém a GAL herdado do Serviço do Exchange. 
    
 _lpc planejadod_
  
> [out] Um ponteiro para a contagem de byte do identificador de entrada da lista de endereços global.
    
 _lppeid_
  
> [out] Um ponteiro para o identificador de entrada da lista de endereços global. Isso deve ser liberado usando [MAPIFreeBuffer](mapifreebuffer.md).
    

