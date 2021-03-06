---
title: Alocando e liberando memória em MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e238f6bc-e9f6-4ea4-a2e4-ff5da2a04bd5
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 68250c5cbeaa366ed4555bb469c4e68d62302f28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419664"
---
# <a name="allocating-and-freeing-memory-in-mapi"></a>Alocando e liberando memória em MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Além de especificar como alocar e liberar memória, o MAPI define um modelo para saber quando a memória passada entre o método de interface pública e as chamadas de função de API devem ser liberadas. O modelo só se aplica à memória alocada para parâmetros que não são ponteiros para interfaces, como cadeias de caracteres e ponteiros para estruturas. Ponteiros de interface usam o mecanismo de contagem de referência implementado por **meio de IUnknown**. Ao alocar e liberar memória não relacionada a MAPI internamente em um aplicativo cliente ou provedor de serviços, use qualquer mecanismo que faça sentido. 
  
O modelo define parâmetros como um dos três tipos. Eles podem ser parâmetros de entrada, definidos pelo chamador com informações a serem usadas pela função ou método chamado, parâmetros de saída, definidos pela função ou método chamado e retornados ao chamador, ou parâmetros de saída de entrada, uma combinação dos dois tipos. Os parâmetros de saída são frequentemente ponteiros para dados ou ponteiros para ponteiros para dados. Embora a função chamada seja responsável por alocar os dados para parâmetros de saída, o chamador aloca a memória para o ponteiro. 
  
As regras para alocar e liberar memória para esses tipos de parâmetros são explicadas na tabela a seguir.
  
|**Tipo**|**Alocação de memória**|**Liberação de memória**|
|:-----|:-----|:-----|
|Input  <br/> |O chamador é responsável e pode usar qualquer mecanismo.  <br/> |O chamador é responsável e pode usar qualquer mecanismo.  <br/> |
|Saída  <br/> |Função chamada é responsável e deve usar **MAPIAllocateBuffer**. Para obter mais informações, [consulte MAPIAllocateBuffer](mapiallocatebuffer.md).  <br/> |O chamador é responsável e deve usar **MAPIFreeBuffer**. Para obter mais informações, [consulte MAPIFreeBuffer](mapifreebuffer.md).  <br/> |
|Entrada-saída  <br/> |O chamador é responsável pela alocação inicial e a função chamada pode realocar, se necessário, usando **MAPIAllocateBuffer**.  <br/> |A função chamada é responsável pela liberação inicial se a realocação for necessária. O chamador deve liberar o valor de retorno final.  <br/> |
   
Durante as condições de falha, os implementadores de métodos de interface precisam prestar atenção aos parâmetros de saída e saída, pois o chamador geralmente não tem como limpá-los. Se um erro for retornado, cada parâmetro de saída ou saída de entrada deverá ser deixado no valor inicializado pelo chamador ou definido como um valor que possa ser limpo sem qualquer ação por parte do chamador. Por exemplo, um parâmetro de ponteiro de saída deve ser deixado como estava na entrada ou pode  `void ** ppv` ser definido como NULL (  `*ppv = NULL` ).
  

