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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 2c5d4ec8381d6614cc2bc92fb0a762b068a97a81
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766624"
---
# <a name="freepadrlist"></a>FreePadrlist

  
  
**Aplica-se a**: Outlook 
  
Destruir uma estrutura [ADRLIST](adrlist.md) e libera a memória associada, incluindo a memória alocada para todos os conjuntos de membro e estruturas. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapiutil.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
void FreePadrlist(
  LPADRLIST padrlist
);
```

## <a name="parameters"></a>Par�metros

 _padrlist_
  
> [in] Ponteiro para a estrutura **ADRLIST** para destruídos. 
    
## <a name="return-value"></a>Valor retornado

Nenhum.
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como parte da sua implementação do **FreePadrlist**, MAPI chama a função [MAPIFreeBuffer](mapifreebuffer.md) para liberar todas as entradas na estrutura de **ADRLIST** antes de liberar a estrutura completa. Portanto, todas as entradas de tais devem ter seguido as regras de alocação para a estrutura [ADRLIST](adrlist.md) , usando um indivíduo [MAPIAllocateBuffer](mapiallocatebuffer.md) chamadas para cada matriz de membro e estrutura. 
  
Para obter mais informações sobre a alocação de memória para as estruturas **ADRLIST** e **SRowSet** , consulte [Gerenciar memória para ADRLIST e estruturas de SRowSet](managing-memory-for-adrlist-and-srowset-structures.md). 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIABFunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI usa o método **FreePadrlist** para liberar uma estrutura ADRLIST que tenha sido criada para adicionar um endereço único a uma mensagem.  <br/> |
   
## <a name="see-also"></a>Confira também



[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

