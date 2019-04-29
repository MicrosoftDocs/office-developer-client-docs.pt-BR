---
title: HrSzFromEntryID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrSzFromEntryID
api_type:
- COM
ms.assetid: 5e3ed6b2-8eaf-44ab-bc6a-d3faabe84a93
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4020a9161a51994ebe5b7e339d26f7612ad47361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411551"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Codifica um identificador de entrada em uma cadeia de caracteres ASCII. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parâmetros

 _cb_
  
> no Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _pentry_ . 
    
 _pentry_
  
> no Ponteiro para uma [](entryid.md) estrutura ENTRYID que contém o identificador de entrada a ser codificado. 
    
 _psz_
  
> bota Ponteiro para a cadeia de caracteres ASCII retornada.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As funções [HrEntryIDFromSz](hrentryidfromsz.md) e **HrSzFromEntryID** fornecem conversão entre a cadeia de caracteres e os formatos binários de identificadores de entrada. Com o MAPI, você deve usar estruturas com dados binários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrSzFromEntryID** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

