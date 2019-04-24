---
title: Gerenciando memória no MAPI
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
  
Saber como e quando alocar e liberar memória é uma parte importante da programação com MAPI. O MAPI fornece funções e macros que o cliente ou provedor de serviços pode usar para gerenciar a memória de forma consistente. As três funções são as seguintes:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Quando os clientes e provedores de serviços usam essas funções, o problema de quem "é proprietário", ou seja, é o que sabe como liberar — um bloco específico de memória é eliminado. Um cliente que chama um método de provedor de serviços não precisa passar um buffer grande o suficiente para conter um valor de retorno de qualquer tamanho. O provedor de serviços pode simplesmente alocar a quantidade apropriada de memória usando o **MAPIAllocateBuffer** e, se necessário, **MAPIAllocateMore**e o cliente pode liberá-lo mais tarde, usando o **MAPIFreeBuffer**, independentemente do serviço provedor. 
  
As macros de memória são usadas para alocar estruturas ou matrizes de estruturas de um tamanho específico. Os clientes e provedores de serviços devem usar essas macros em vez de alocar a memória manualmente. Por exemplo, se um cliente precisar executar o processamento de resolução de nome em uma lista de destinatários com três entradas, a macro **SizedADRLIST** poderá ser usada para criar uma estrutura **das ADRLIST** para passar para **IAddrBook:: ResolveName** com o número correto de Membros **ADRENTRY** . Todas as macros de memória são definidas no MAPIDEFS. Arquivo de cabeçalho H. Essas macros são: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI também suporta o uso da interface COM [IMalloc](https://msdn.microsoft.com/library/ms678425%28VS.85%29.aspx) para gerenciamento de memória. Os provedores de serviço recebem um ponteiro de interface **IMalloc** por MAPI no momento da inicialização e também podem recuperar um por meio da função [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . A principal vantagem de usar os métodos **IMalloc** para gerenciar a memória sobre as funções MAPI é que, com os métodos com, é possível realocar um buffer existente. As funções de memória MAPI não oferecem suporte à realocação. 
  

