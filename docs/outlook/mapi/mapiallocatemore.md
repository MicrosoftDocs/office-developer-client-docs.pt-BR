---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357313"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Aloca um buffer de memória que está vinculado a outro buffer anteriormente alocado com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _cbSize_
  
> no Tamanho, em bytes, do novo buffer a ser alocado. 
    
 _lpObject_
  
> no Ponteiro para um buffer MAPI existente alocado usando **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> bota Ponteiro para o buffer retornado e recentemente alocado.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou um ponteiro para a memória solicitada.
    
## <a name="remarks"></a>Comentários

Durante o processamento de chamada **MAPIAllocateMore** , a implementação de chamada adquire um bloco de memória do sistema operacional. O buffer de memória é alocado em um endereço de byte par numerado. Nas plataformas nas quais o acesso inteiro longo é mais eficiente, o sistema operacional aloca o buffer em um endereço cujo tamanho em bytes é um múltiplo de quatro. 
  
A única maneira de liberar um buffer alocado com o **MAPIAllocateMore** é passar o ponteiro de buffer especificado no parâmetro _lpObject_ para a função [MAPIFreeBuffer](mapifreebuffer.md) . O link entre os buffers de memória alocados com o [MAPIAllocateBuffer](mapiallocatebuffer.md) e o **MAPIAllocateMore** permite que o **MAPIFreeBuffer** libere os dois buffers com uma única chamada. 
  

