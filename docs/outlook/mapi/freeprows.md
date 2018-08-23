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
ms.openlocfilehash: 0686cee9bf6fa47332f75f99e1d2a2d35cb7e7fb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578021"
---
# <a name="freeprows"></a>FreeProws

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Destruir uma estrutura [SRowSet](srowset.md) e libera a memória associada, incluindo a memória alocada para todos os conjuntos de membro e estruturas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
void FreeProws(
  LPSRowSet prows
);
```

## <a name="parameters"></a>Parâmetros

 _prows_
  
> [in] Ponteiro para a estrutura de **SRowSet** para destruídos. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como parte da sua implementação do **FreeProws**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas na estrutura de **SRowSet** antes de liberar a estrutura completa. Portanto, todas as entradas de tais devem ter seguido as regras de alocação para a estrutura [SRowSet](srowset.md) , usando um indivíduo [MAPIAllocateBuffer](mapiallocatebuffer.md) chamadas para cada matriz de membro e estrutura. 
  
Para obter mais informações sobre a alocação de memória para as estruturas **ADRLIST** e **SRowSet** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |DwThreadFuncLoadTable  <br/> |MFCMAPI usa o método **FreeProws** para liberar uma estrutura SRowSet contendo as linhas da tabela que estão sendo processadas.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

