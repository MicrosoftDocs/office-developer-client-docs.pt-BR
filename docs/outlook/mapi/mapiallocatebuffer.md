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
ms.openlocfilehash: 0520b219c87207a54555ba74050761f6ecc4854a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579596"
---
# <a name="mapiallocatebuffer"></a>MAPIAllocateBuffer

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca um buffer de memória. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _cbSize_
  
> [in] Tamanho, em bytes, do buffer a ser alocado. 
    
 _lppBuffer_
  
> [out] Ponteiro para o buffer alocado retornado.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o buffer de memória solicitada.
    
## <a name="remarks"></a>Comentários

Processamento de chamadas durante **MAPIAllocateBuffer** , a implementação chamando adquire um bloco de memória do sistema operacional. O buffer de memória é alocado em um endereço de pares de byte. Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro. 
  
Chamar as versões de função [MAPIFreeBuffer](mapifreebuffer.md) o buffer de memória alocado por **MAPIAllocateBuffer**, chamando-se a função [MAPIAllocateMore](mapiallocatemore.md) e qualquer buffers vinculadas a ela, quando a memória não é mais necessária. 
  
## <a name="see-also"></a>Confira também



[MAPIReallocateBuffer](mapireallocatebuffer.md)

