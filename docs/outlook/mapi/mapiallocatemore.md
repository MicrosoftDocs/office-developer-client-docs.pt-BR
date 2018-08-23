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
ms.openlocfilehash: 0e6226dd0fc9c04070ed3d1dda1770f77fbc585c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583005"
---
# <a name="mapiallocatemore"></a>MAPIAllocateMore

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

