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
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767989"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Aplica-se a**: Outlook 
  
Aloca um buffer de memória que é vinculado a outro buffer anteriormente alocado com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) . 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapix.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a>Parâmetros

 _cbSize_
  
> [in] Tamanho, em bytes, do buffer de novo a ser alocado. 
    
 _lpObject_
  
> [in] Ponteiro para um buffer MAPI existente alocado usando **MAPIAllocateBuffer**.
    
 _lppBuffer_
  
> [out] Ponteiro para o retornados recentemente alocado buffer.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou um ponteiro para a memória solicitada.
    
## <a name="remarks"></a>Comentários

Processamento de chamadas durante **MAPIAllocateMore** , a implementação chamando adquire um bloco de memória do sistema operacional. O buffer de memória é alocado em um endereço de pares de byte. Em plataformas onde o acesso de inteiro longo é mais eficiente, o sistema operacional aloca o buffer de um endereço cujo tamanho em bytes é um múltiplo de quatro. 
  
Passe o ponteiro de buffer especificado no parâmetro _lpObject_ para a função [MAPIFreeBuffer](mapifreebuffer.md) é a única maneira de liberar um buffer alocado com **MAPIAllocateMore** . O vínculo entre os buffers de memória alocada com [MAPIAllocateBuffer](mapiallocatebuffer.md) e **MAPIAllocateMore** permite **MAPIFreeBuffer** ao lançamento de ambos os buffers com uma única chamada. 
  

