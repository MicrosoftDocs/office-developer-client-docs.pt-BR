---
title: HrEntryIDFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrEntryIDFromSz
api_type:
- COM
ms.assetid: 14c171ec-0aec-43ab-8be8-e6bc0ce28a58
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a524a7eb40c33d6de2f64cd5373c9a39a8a1e3df
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565295"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recria um identificador de entrada de sua codificação ASCII. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parâmetros

 _SZ_
  
> [in] Ponteiro para a cadeia de caracteres ASCII do qual criar um identificador de entrada. 
    
 _PCB_
  
> [out] Ponteiro para o tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _ppentry_ . 
    
 _ppentry_
  
> [out] Ponteiro para um ponteiro para a estrutura [ENTRYID](entryid.md) retornado que contém o novo identificador de entrada. 
    
## <a name="return-value"></a>Valor retornado

S_OK
  
> A recriação foi bem-sucedida.
    
MAPI_E_INVALID_ENTRYID
  
> A identificação de entrada era inválida.
    
## <a name="remarks"></a>Comentários

As funções **HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e formatos binários de identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

