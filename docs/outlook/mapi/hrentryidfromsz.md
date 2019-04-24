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
ms.openlocfilehash: ac59aeb3d650c0fbeb5bcdb580e0401cbab58ee6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347807"
---
# <a name="hrentryidfromsz"></a>HrEntryIDFromSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recria um identificador de entrada da codificação ASCII. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente  <br/> |
   
```cpp
HRESULT HrEntryIDFromSz(
  LPSTR sz,
  ULONG FAR * pcb,
  LPENTRYID FAR * ppentry
);
```

## <a name="parameters"></a>Parâmetros

 _v_
  
> no Ponteiro para a cadeia de caracteres ASCII da qual criar um identificador de entrada. 
    
 _PCB_
  
> bota Ponteiro para o tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _ppentry_ . 
    
 _ppentry_
  
> bota Ponteiro para um ponteiro para a estrutura [EntryID](entryid.md) retornada que contém o novo identificador de entrada. 
    
## <a name="return-value"></a>Valor de retorno

S_OK
  
> A recreação foi bem-sucedida.
    
MAPI_E_INVALID_ENTRYID
  
> A identificação de entrada era inválida.
    
## <a name="remarks"></a>Comentários

As funções **HrEntryIDFromSz** e [HrSzFromEntryID](hrszfromentryid.md) fornecem conversão entre a cadeia de caracteres e os formatos binários de identificadores de entrada. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

A função **HrEntryIDFromSz** aloca memória para a cadeia de caracteres ASCII usando a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  

