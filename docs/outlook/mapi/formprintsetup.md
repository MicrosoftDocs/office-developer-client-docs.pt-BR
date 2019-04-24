---
title: FORMPRINTSETUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FORMPRINTSETUP
api_type:
- COM
ms.assetid: 6e82fe94-47bd-4a25-b25b-0ab6fe2db274
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c2b9176e21341ef28e6f0bc007757b097a05daee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327283"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Descreve as informações de configuração de impressão para o objeto Form. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiform. h  <br/> |
   
```cpp
typedef struct
{
  ULONG ulFlags;
  HDEVMODE hDevMode;
  HDEVNAMES hDevNames;
  ULONG ulFirstPageNumber;
  ULONG ulFPrintAttachments;
} FORMPRINTSETUP, FAR * LPFORMPRINTSETUP;

```

## <a name="members"></a>Membros

 **ulFlags**
  
> Bitmask de sinalizadores que controla o tipo de cadeia de caracteres. O seguinte sinalizador pode ser usado:
    
MAPI_UNICODE 
  
> As cadeias de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estarão no formato ANSI.
    
 **hDevmode**
  
> Identificador para o modo da impressora.
    
 **hDevnames**
  
> Identificador para o caminho da impressora.
    
 **ulFirstPageNumber**
  
> Número de página da primeira página a ser impressa.
    
 **ulFPrintAttachments**
  
> Sinalizador que indica se há anexos a serem impressos. Se houver anexos para impressão, o membro **ulFPrintAttachments** será definido como 1. Se não houver anexos a serem impressos, será definido como 0. 
    
## <a name="remarks"></a>Comentários

A estrutura **FORMPRINTSETUP** é usada para descrever as informações de configuração de impressão de um objeto Form. Implementações de [IMAPIViewContext:: GetPrintSetup](imapiviewcontext-getprintsetup.md) preencher a estrutura **FORMPRINTSETUP** e retorná-lo no conteúdo do parâmetro de saída _lppFormPrintSetup_ de **GetPrintSetup**.
  
Se o sinalizador MAPI_UNICODE for passado no parâmetro _parâmetroulflags_ de **GetPrintSetup**, as cadeias de caracteres referenciadas pelos membros **hDevmode** e **hDevnames** devem estar no formato Unicode. Caso contrário, as cadeias de caracteres devem estar no formato ANSI. 
  
Os visualizadores de formulários que implementam o **IMAPIViewContext** devem alocar a estrutura **FORMPRINTSETUP** usando a função de alocador MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), mas alocar os membros individuais, **hDevMode** e **hDevNames**, com a função [GlobalAlloc](https://go.microsoft.com/fwlink/?LinkId=132110)do Windows. O lançamento da memória é tratado de forma semelhante. Os membros **hDevMode** e **hDevNames** devem ser liberados usando a função [GlobalFree](https://go.microsoft.com/fwlink/?LinkId=132108) do Windows, enquanto a estrutura **FORMPRINTSETUP** deve ser liberada com a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Estruturas MAPI](mapi-structures.md)

