---
title: Gerenciamento de memória para as estruturas ADRLIST e SRowSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d009f6b6-d151-4d52-b7cc-a15127142354
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ef20cf8460aa7d3d160208109e42b2de66658d54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589725"
---
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gerenciando a memória para as estruturas ADRLIST e SRowSet"

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O requisito de alocar memória todos para um buffer sempre que possível, com uma única chamada **MAPIAllocateBuffer** não se aplica ao usar a lista de endereços ou estruturas **ADRLIST**e **SRowSet**ou conjunto de linhas. 
  
Essas duas estruturas são exceções às regras padrão de alocação e da liberação de memória. Elas contêm vários níveis de estruturas e são projetadas para permitir que membros individuais sejam adicionadas ou removidas. Portanto, cada propriedade deve ser uma alocação separada. 

Onde a maioria das estruturas são liberadas com uma chamada de **MAPIFreeBuffer**, cada entrada individual em uma estrutura **ADRLIST** ou **SRowSet** devem ser liberada com sua própria chamada para **MAPIFreeBuffer** ou uma única chamada para **FreeProws** ou ** FreePadrlist**. Para obter mais informações, consulte [MAPIFreeBuffer](mapifreebuffer.md), [ADRLIST](adrlist.md)e [SRowSet](srowset.md). 

**FreeProws** e **FreePadrlist** são funções fornecidas pelo MAPI para simplificar o dispensando dessas estruturas de dados. Para obter mais informações, consulte [FreeProws](freeprows.md) e [FreePadrlist](freepadrlist.md). **FreePadrlist** libera a memória para a estrutura **ADRLIST** plus todos os respectivos memória para os membros de estrutura; **FreeProws** faz o mesmo para a estrutura **SRowSet** . 
  
O diagrama a seguir mostra o layout de uma estrutura de dados **ADRLIST** , indicando as alocações de memória separado necessárias. As caixas cinzas mostram a memória que pode ser alocada e lançada com uma chamada. 
  
**ADRLIST memory allocation**
  
![Alocação de memória ADRLIST] (media/amapi_52.gif "Alocação de memória ADRLIST")
  
## <a name="see-also"></a>Confira também

- [Gerenciando memória nos MAPI](managing-memory-in-mapi.md)

