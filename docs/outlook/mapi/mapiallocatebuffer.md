---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357306"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca um buffer de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _cbSize_
  
> no Tamanho, em bytes, do buffer a ser alocado. 
    
 _lppBuffer_
  
> bota Ponteiro para o buffer alocado retornado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o buffer de memória solicitado.
    
## <a name="remarks"></a>Comentários

Durante o processamento de chamada **MAPIAllocateBuffer** , a implementação de chamada adquire um bloco de memória do sistema operacional. O buffer de memória é alocado em um endereço de byte par numerado. Nas plataformas nas quais o acesso inteiro longo é mais eficiente, o sistema operacional aloca o buffer em um endereço cujo tamanho em bytes é um múltiplo de quatro. 
  
Chamar a função [MAPIFreeBuffer](mapifreebuffer.md) libera o buffer de memória alocado por **MAPIAllocateBuffer**, chamando a função [MAPIAllocateMore](mapiallocatemore.md) e todos os buffers vinculados a ele, quando a memória não é mais necessária. 
  
## <a name="see-also"></a>Confira também



[MAPIReallocateBuffer](mapireallocatebuffer.md)

