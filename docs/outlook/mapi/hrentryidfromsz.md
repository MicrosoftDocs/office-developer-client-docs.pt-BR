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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2b7ef789c80f85f3539ec3bbd0caf4a8adc50f3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766789"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

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
    
## <a name="remarks"></a>Coment�rios

As funções **HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e formatos binários de identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

