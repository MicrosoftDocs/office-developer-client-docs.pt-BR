---
title: FreePadrlist
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FreePadrlist
api_type:
- COM
ms.assetid: ca8fbac6-b6f1-46ab-90a1-fc16f0d5824c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 95c2e52760bd7d65351b4dd2091b68a43cd2f97c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328032"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Destrói uma estrutura [das ADRLIST](adrlist.md) e libera a memória associada, incluindo a memória alocada para todas as matrizes e estruturas de membros. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Parâmetros

 _padrlist_
  
> no Ponteiro para a estrutura **das ADRLIST** a ser destruído. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como parte de sua implementação do **FreePadrlist**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas da estrutura **das ADRLIST** antes de liberar a estrutura completa. Portanto, todas as entradas devem ter seguido as regras de alocação para a estrutura [das ADRLIST](adrlist.md) , usando uma chamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz de membros e estrutura. 
  
Para obter mais informações sobre a alocação de memória para as estruturas **das ADRLIST** e **SRowSet** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIABFunctions. cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o método **FreePadrlist** para liberar uma estrutura das ADRLIST que foi criada para adicionar um endereço one-off a uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

