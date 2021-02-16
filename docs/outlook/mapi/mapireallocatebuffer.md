---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435282"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Realoca um buffer de memória. Ele é usado com a [função MAPIAllocateBuffer.](mapiallocatebuffer.md) 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |omapix.h  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a>Parâmetros

 _lpv_
  
> Um ponteiro para a memória a ser realocada.
    
 _ulSize_
  
> O tamanho, em bytes, do buffer a ser alocado.
    
 _lppv_
  
> Um ponteiro para o buffer alocado retornado.
    
## <a name="remarks"></a>Comentários

 **MAPIReallocateBuffer** aloca um novo bloco de memória do tamanho solicitado e copia o conteúdo do buffer que é passado para esse novo bloco de memória. Se o bloco de memória passado contiver ponteiros internos, os ponteiros não mudarão para corresponder ao novo local. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)

