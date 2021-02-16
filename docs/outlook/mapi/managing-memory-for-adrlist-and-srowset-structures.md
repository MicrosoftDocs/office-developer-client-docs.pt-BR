---
title: Gerenciar memória das estruturas ADRLIST e SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a5636cad7cad23bb5114bdbd34aff48c3639773b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407862"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gerenciando memória para estruturas ADRLIST e SRowSet"

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O requisito de alocar toda a memória para um buffer sempre que possível com uma única chamada **MAPIAllocateBuffer** não se aplica ao usar a lista de endereços, ou **ADRLIST** e conjunto de linhas, ou **SRowSet**, estruturas. 
  
Essas duas estruturas são exceções às regras padrão para alocar e liberar memória. Eles contêm vários níveis de estruturas e são projetados para permitir que membros individuais sejam adicionados ou removidos. Portanto, cada propriedade deve ser uma alocação separada. 

Onde a maioria das estruturas são liberadas com uma chamada para **MAPIFreeBuffer**, cada entrada individual em uma **estrutura ADRLIST** ou **SRowSet** deve ser liberada com sua própria chamada para **MAPIFreeBuffer** ou uma única chamada para **FreeProws** ou **FreePadrlist**. Para obter mais informações, [consulte MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)e [SRowSet](srowset.md). 

**FreeProws** e **FreePadrlist** são funções fornecidas pelo MAPI para simplificar a liberação dessas estruturas de dados. Para obter mais informações, [consulte FreeProws](freeprows.md) e [FreePadrlist](freepadrlist.md). **FreePadrlist** libera a memória para a estrutura **ADRLIST,** além de toda a memória associada para os membros da estrutura; **FreeProws** faz o mesmo para a **estrutura SRowSet.** 
  
O diagrama a seguir mostra o layout de uma estrutura de dados **ADRLIST,** indicando as alocações de memória separadas necessárias. As caixas cinza mostram a memória que pode ser alocada e liberada com uma chamada. 
  
**ADRLIST memory allocation**
  
![Alocação de memória ADRLIST](media/amapi_52.gif "da ADRLIST")
  
## <a name="see-also"></a>Confira também

- [Gerenciando memória no MAPI](managing-memory-in-mapi.md)

