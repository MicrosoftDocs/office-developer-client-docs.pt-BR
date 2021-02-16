---
title: Gerenciando memória em MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 66489c09be641d8fe9ae5f3ffff46a6d5004f473
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32298093"
---
# <a name="managing-memory-in-mapi"></a>Gerenciando memória no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Saber como e quando alocar e liberar memória é uma parte importante da programação com MAPI. MAPI provides both functions and macros that your client or service provider can use to manage memory in a consistent way. As três funções são as seguinte:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Quando os clientes e provedores de serviços usam essas funções, o problema de quem "possui" — ou seja, sabe como liberar — um determinado bloco de memória é eliminado. Um cliente que chama um método de provedor de serviços não precisa passar um buffer grande o suficiente para manter um valor de retorno de qualquer tamanho. O provedor de serviços pode simplesmente alocar a quantidade adequada de memória usando **MAPIAllocateBuffer** e, se necessário, **MAPIAllocateMore**, e o cliente pode liberá-lo posteriormente usando **MAPIFreeBuffer**, independentemente do provedor de serviços. 
  
As macros de memória são usadas para alocar estruturas ou matrizes de estruturas de um tamanho específico. Os clientes e provedores de serviços devem usar essas macros em vez de alocar a memória manualmente. Por exemplo, se um cliente precisar executar o processamento de resolução de nomes em uma lista de destinatários com três entradas, a macro **SizedADRLIST** poderá ser usada para criar uma estrutura **ADRLIST** para passar para **IAddrBook::ResolveName** com o número correto de membros **ADRENTRY.** Todas as macros de memória são definidas em MAPIDEFS. Arquivo de header H. Essas macros são: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI also supports the use of the COM interface [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) for memory management. Os provedores de serviços receberão um ponteiro de interface **IMalloc** por MAPI no momento da inicialização e também podem recuperar um por meio da função [MAPIGetDefaultMalloc.](mapigetdefaultmalloc.md) A principal vantagem de usar os métodos **IMalloc** para gerenciar memória sobre as funções MAPI é que, com os métodos COM, é possível realocar um buffer existente. As funções de memória MAPI não suportam realocação. 
  

