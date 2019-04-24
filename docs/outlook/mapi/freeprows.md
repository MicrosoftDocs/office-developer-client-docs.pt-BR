---
title: FreeProws
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeProws
api_type:
- HeaderDef
ms.assetid: 0f8f9fc4-4940-4c0a-92cc-2a6409b9a13f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b1109b3201e1b1e4a78c3a0fe0f2eb4d0cd43c05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328011"
---
# <a name="freeprows"></a>FreeProws

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Destrói uma estrutura [SRowSet](srowset.md) e libera a memória associada, incluindo a memória alocada para todas as matrizes e estruturas de membros. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parâmetros

 _prows_
  
> no Ponteiro para a estrutura **SRowSet** a ser destruído. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como parte de sua implementação do **FreeProws**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas da estrutura **SRowSet** antes de liberar a estrutura completa. Portanto, todas as entradas devem ter seguido as regras de alocação para a estrutura [SRowSet](srowset.md) , usando uma chamada [MAPIAllocateBuffer](mapiallocatebuffer.md) individual para cada matriz de membros e estrutura. 
  
Para obter mais informações sobre a alocação de memória para as estruturas **das ADRLIST** e **SRowSet** , consulte [Managing Memory for das ADRLIST and SRowSet structures](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método **FreeProws** para liberar uma estrutura SRowSet contendo linhas da tabela que está sendo processada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

