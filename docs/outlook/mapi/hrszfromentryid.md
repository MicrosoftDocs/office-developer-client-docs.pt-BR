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
ms.openlocfilehash: 1b957c02f331038ee9104f01806720d2f8e0b542
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766806"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Aplica-se a**: Outlook 
  
Codifica um identificador de entrada em uma sequência de caracteres ASCII. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HrSzFromEntryID(
  ULONG cb,
  LPENTRYID pentry,
  LPSTR FAR * psz
);
```

## <a name="parameters"></a>Parâmetros

 _cb_
  
> [in] Tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _pentry_ . 
    
 _pentry_
  
> [in] Ponteiro para uma estrutura [ENTRYID](entryid.md) que contém o identificador de entrada a ser codificada. 
    
 _psz_
  
> [out] Ponteiro para a cadeia de caracteres ASCII retornado.
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="remarks"></a>Comentários

As funções [HrEntryIDFromSz](hrentryidfromsz.md) e **HrSzFromEntryID** fornecem conversão entre a cadeia de caracteres e formatos binários de identificadores de entrada. Com MAPI, você deve usar as estruturas com dados binários. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrSzFromEntryID** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

