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
# <a name="managing-memory-for-adrlist-and-srowset-structures"></a>Gerenciando memória para estruturas das ADRLIST e SRowSet "

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O requisito para alocar toda a memória de um buffer sempre que possível com uma única chamada **MAPIAllocateBuffer** não se aplica ao usar a lista de endereços ou o **das ADRLIST**e o conjunto de linhas ou as estruturas **SRowSet**. 
  
Essas duas estruturas são exceções às regras padrão para alocar e liberar memória. Eles contêm vários níveis de estruturas e foram projetados para permitir que membros individuais sejam adicionados ou removidos. Portanto, cada propriedade deve ser uma alocação separada. 

Onde a maioria das estruturas é liberada com uma chamada para **MAPIFreeBuffer**, cada entrada individual em uma estrutura **das ADRLIST** ou **SRowSet** deve ser liberada com sua própria chamada para **MAPIFreeBuffer** ou uma única chamada para **FreeProws** ou ** FreePadrlist**. Para obter mais informações, consulte [MAPIFreeBuffer](mapifreebuffer.md), [das ADRLIST](adrlist.md)e [SRowSet](srowset.md). 

**FreeProws** e **FreePadrlist** são funções fornecidas pelo MAPI para simplificar a liberação dessas estruturas de dados. Para obter mais informações, consulte [FreeProws](freeprows.md) e [FreePadrlist](freepadrlist.md). **FreePadrlist** libera a memória da estrutura **das ADRLIST** mais toda a memória associada para os membros da estrutura; **FreeProws** faz o mesmo para a estrutura **SRowSet** . 
  
O diagrama a seguir mostra o layout de uma estrutura de dados do **das ADRLIST** , indicando as alocações de memória separadas necessárias. As caixas cinzas mostram a memória que pode ser alocada e liberada com uma chamada. 
  
**ADRLIST memory allocation**
  
![Alocação de memória das ADRLIST] (media/amapi_52.gif "Alocação de memória das ADRLIST")
  
## <a name="see-also"></a>Confira também

- [Gerenciando memória no MAPI](managing-memory-in-mapi.md)

