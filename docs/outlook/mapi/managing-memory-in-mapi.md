---
title: Gerenciando memória nos MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9eee6925-ab91-413e-8907-c747ab4a4bb5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c30aa631e70f8f4be52c2fd42dd6bfad900f379e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566156"
---
# <a name="managing-memory-in-mapi"></a>Gerenciando memória nos MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Saber como e quando alocar e liberar memória é uma parte importante da programação com MAPI. MAPI fornece funções e macros que seu provedor de cliente ou serviço pode usar para gerenciar memória de maneira consistente. As três funções são:
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
Quando os clientes e provedores de serviços usam essas funções, o problema de "responsável" — ou seja, sabe como liberar — um bloco de memória particular foram eliminado. Um cliente chamar um método de provedor de serviço não precisa passar um grande o suficiente para armazenar um valor de retorno de qualquer tamanho do buffer. O provedor de serviços pode simplesmente alocar a quantidade apropriada de memória usando **MAPIAllocateBuffer** e, se necessário, **MAPIAllocateMore**e o cliente podem posteriormente liberá-la à vontade usando **MAPIFreeBuffer**, independente do serviço provedor. 
  
As macros de memória são usadas para alocar estruturas ou matrizes de estruturas de um determinado tamanho. Provedores de serviços e clientes devem usar estas macros em vez de alocar a memória manualmente. Por exemplo, se um cliente precisar realizar a resolução de nomes de processamento em uma lista de destinatários com três entradas, a macro de **SizedADRLIST** pode ser usada para criar uma estrutura **ADRLIST** a serem passados para **IAddrBook::ResolveName** com o número correto de Membros do **ADRENTRY** . Todas as macros de memória são definidas no MAPIDEFS. Arquivo de cabeçalho H. Estas macros são: 
  
|||
|:-----|:-----|
|[SizedADRLIST](sizedadrlist.md) <br/> |[SizedDtblPage](sizeddtblpage.md) <br/> |
|[SizedDtblButton](sizeddtblbutton.md) <br/> |[SizedENTRYID](sizedentryid.md) <br/> |
|[SizedDtblCheckBox](sizeddtblcheckbox.md) <br/> |[SizedSPropProblemArray](sizedspropproblemarray.md) <br/> |
|[SizedDtblComboBox](sizeddtblcombobox.md) <br/> |[SizedSPropTagArray](sizedsproptagarray.md) <br/> |
|[SizedDtblEdit](sizeddtbledit.md) <br/> |[SizedSRowSet](sizedsrowset.md) <br/> |
|[SizedDtblGroupBox](sizeddtblgroupbox.md) <br/> |[SizedSSortOrderSet](sizedssortorderset.md) <br/> |
|[SizedDtblLabel](sizeddtbllabel.md) <br/> | <br/> |
   
MAPI também suporta o uso da interface COM [IMalloc](http://msdn.microsoft.com/en-us/library/ms678425%28VS.85%29.aspx) para gerenciamento de memória. Provedores de serviço recebem um ponteiro de interface **IMalloc** por MAPI em tempo de inicialização e também podem recuperar um por meio da função [MAPIGetDefaultMalloc](mapigetdefaultmalloc.md) . A principal vantagem de usar os métodos **IMalloc** para gerenciar memória sobre as funções MAPI é que com os métodos COM é possível realocar um buffer existente. As funções de memória MAPI não dão suporte a realocação. 
  

