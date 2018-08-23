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
ms.openlocfilehash: 366208b8288aeb61bf1bb78f2c9f10b400a3dc26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567591"
---
# <a name="hrszfromentryid"></a>HrSzFromEntryID

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

