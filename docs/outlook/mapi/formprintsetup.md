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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ff46c58fbb352d56ae3df09d6949cdd5f614673f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766600"
---
# <a name="formprintsetup"></a>FORMPRINTSETUP

  
  
**Aplica-se a**: Outlook 
  
Descreve as informações de configuração de impressão para o objeto de formulário. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |MAPIForm.h  <br/> |
   
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
  
> Bitmask dos sinalizadores que controla o tipo das cadeias de caracteres. O seguinte sinalizador pode ser usado:
    
MAPI_UNICODE 
  
> As cadeias de caracteres estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, as cadeias de caracteres estão no formato ANSI.
    
 **hDevmode**
  
> Identificador para o modo da impressora.
    
 **hDevnames**
  
> Identificador para o caminho da impressora.
    
 **ulFirstPageNumber**
  
> Número de página da primeira página a ser impressa.
    
 **ulFPrintAttachments**
  
> Sinalizador que indica se há anexos a ser impresso. Se houver anexos para imprimir, o membro **ulFPrintAttachments** estiver definido como 1. Se não houver nenhum anexo para imprimir, ela é definida como 0. 
    
## <a name="remarks"></a>Coment�rios

A estrutura **FORMPRINTSETUP** é usada para descrever as informações de configuração de impressão de um objeto form. Implementações de [IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md) preencham a estrutura **FORMPRINTSETUP** e retorná-lo no conteúdo do parâmetro de saída _lppFormPrintSetup_ de **GetPrintSetup**.
  
Se o sinalizador MAPI_UNICODE é passado no parâmetro _ulFlags_ do **GetPrintSetup**, as cadeias de caracteres referenciadas pelos membros **hDevmode** e **hDevnames** devem estar no formato Unicode. Caso contrário, as cadeias de caracteres devem estar no formato ANSI. 
  
Visualizadores de formulário implementando **IMAPIViewContext** devem alocar a estrutura **FORMPRINTSETUP** usando a função de alocador MAPI [MAPIAllocateBuffer](mapiallocatebuffer.md), mas alocar os membros individuais, **hDevMode** e **hDevNames**, com a função do Windows [GlobalAlloc](http://go.microsoft.com/fwlink/?LinkId=132110). A versão de memória é tratada da mesma forma. Os membros **hDevMode** e **hDevNames** devem ser liberados usando a função [GlobalFree](http://go.microsoft.com/fwlink/?LinkId=132108) do Windows enquanto a estrutura **FORMPRINTSETUP** deve ser liberada com a função [MAPIFreeBuffer](mapifreebuffer.md) . 
  
## <a name="see-also"></a>Confira também



[IMAPIViewContext::GetPrintSetup](imapiviewcontext-getprintsetup.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)


[Estruturas MAPI](mapi-structures.md)

