---
title: Alocar e liberar memória no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2ec5c2604c72d41078aa467764463e2659c62e65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587940"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Alocar e liberar memória no MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além de especificar como alocar e liberar memória, MAPI define um modelo para saber quando memória passadas entre o método de interface pública e a função API chamadas devem ser liberadas. O modelo se aplica somente a memória alocada para os parâmetros que não são ponteiros para interfaces, como cadeias de caracteres e ponteiros para estruturas. Ponteiros de interface usam a mecanismo implementado através de **IUnknown**de contagem de referência. Quando alocar e liberar non-MAPI relacionadas a memória internamente dentro de um aplicativo cliente ou o provedor de serviço, use qualquer mecanismo faz sentido. 
  
O modelo define os parâmetros como um dos três tipos. Eles podem ser inseridos parâmetros, definidos pelo chamador com as informações a serem usados pelo método, ou uma função chamada parâmetros de saída, definido pela função chamada ou método e retornada para o chamador ou parâmetros de entrada e saída, uma combinação dos dois tipos. Parâmetros de saída são frequentemente ponteiros para dados ou ponteiros para ponteiros para dados. Embora a função chamada é responsável por alocar os dados para os parâmetros de saída, o chamador aloca a memória para o ponteiro. 
  
As regras de alocação e da liberação de memória para esses tipos de parâmetros são explicadas na tabela a seguir.
  
|**Tipo**|**Alocação de memória**|**Versão de memória**|
|:-----|:-----|:-----|
|Entrada  <br/> |Chamador é responsável e pode usar qualquer mecanismo.  <br/> |Chamador é responsável e pode usar qualquer mecanismo.  <br/> |
|Saída  <br/> |Função chamada é responsável e deve usar **MAPIAllocateBuffer**. Para obter mais informações, consulte [MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |Chamador é responsável e deve usar **MAPIFreeBuffer**. Para obter mais informações, consulte [MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Entrada e saída  <br/> |Chamador é responsável para a alocação inicial e a função chamada podem realocar se necessário usando **MAPIAllocateBuffer**.  <br/> |Função chamada é responsável por dispensando inicial se realocação é necessária. Chamador deve liberar o valor de retorno final.  <br/> |
   
Durante as condições de falha, implementadores métodos da interface precisam preste atenção aos parâmetros de entrada e saída e de saída, porque o chamador geralmente não tem como limpá-los. Se um erro será retornado, em seguida, cada saída ou o parâmetro de entrada e saída deve seja ser deixado no valor inicializado pelo chamador ou definida como um valor que pode ser limpos sem qualquer ação por parte do chamador. Por exemplo, um ponteiro-parâmetro de saída do `void ** ppv` deverá permanecer como ela foi na entrada ou pode ser definido como NULL ( `*ppv = NULL`).
  

