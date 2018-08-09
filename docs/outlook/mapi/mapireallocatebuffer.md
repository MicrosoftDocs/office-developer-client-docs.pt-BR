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
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768014"
---
# <a name="mapireallocatebuffer"></a>MAPIReallocateBuffer

  
  
**Aplica-se a**: Outlook 
  
Realoca um buffer de memória. Ele é usado com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |omapix.h  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
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
  
> Um ponteiro para a memória sejam realocados.
    
 _ulSize_
  
> O tamanho, em bytes, do buffer a ser alocado.
    
 _lppv_
  
> Um ponteiro para o buffer alocado retornado.
    
## <a name="remarks"></a>Comentários

 **MAPIReallocateBuffer** aloca um novo bloco de memória do tamanho solicitado e copia o conteúdo do buffer que é passado para este novo bloco de memória. Se o bloco de memória que é passada contém ponteiros internos, não alteram os ponteiros para coincidir com o novo local. 
  
## <a name="see-also"></a>Confira também



[MAPIAllocateBuffer](mapiallocatebuffer.md)

