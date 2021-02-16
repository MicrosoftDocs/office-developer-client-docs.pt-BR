---
title: Implementando um objeto Sink Advise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412104"
---
# <a name="implementing-an-advise-sink-object"></a>Implementando um objeto Sink Advise

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode implementar seus próprios objetos de evento de consultoria ou usar uma função de utilitário, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** cria um objeto sink de alerta com uma implementação de **OnNotify** que invoca uma função de retorno de chamada. 
  
Há vantagens e desvantagens ao usar **HrAllocAdviseSink**. Ele pode salvar o trabalho, mas não fornece controle sobre a contagem de referência do objeto sink de aconselhamento que ele cria. Portanto, os clientes que precisam controlar cuidadosamente a liberação de seus clientes aconselhados ou que têm interdependências entre seu cliente e o cliente devem construir sua própria implementação **IMAPIAdviseSink** e evitar usar o **HrAllocAdviseSink** completamente. 
  
Um cliente implementando seu próprio objeto de alerta deve torná-lo um objeto independente não relacionado a ou dependente de qualquer outro objeto para eliminar possíveis complicações na contagem de referências e na liberação de objetos. No entanto, se você deve implementar seu sink de conselhos como parte de outro objeto ou incluir um ponteiro de fundo para outro objeto como um membro de dados, é recomendável que duas contagens de referência separadas sejam mantidas: uma para o objeto referenciado pelo sink de aconselhação e uma para o sink de consultoria. 
  
Quando a contagem de referência do objeto referenciado cai para zero, todos os seus métodos podem falhar e sua vtable pode ser destruída, mas a memória para o sink de alerta deve permanecer intacta até que sua contagem de referência também cai para zero. Isso significa que o método **Release** do sink de alerta deve rebaixar sua contagem de referência e terminar de destruir o objeto quando essa contagem atingir zero. Se duas contagens de referência separadas não são mantidas, seria fácil destruir inadvertidamente o  sink de consultoria como parte do processo de liberação do objeto que o abrange. 
  
Os clientes **que usam HrAllocAdviseSink** para implementar um sink de alerta devem ter igualmente cuidado para não incluir sua função de retorno de chamada como um método em outro objeto sink de aconselhá-lo. Para clientes C++, é tentador fazer isso e passar  _o ponteiro_ como um parâmetro. Essa é uma estratégia perigosa porque os clientes normalmente liberam um objeto quando sua contagem de referência atinge zero. Liberar a memória para o objeto de evento de aconselhagem poderia tornar  _o ponteiro_ inválido. 
  
Dependendo do tipo de evento e da fonte de conselhos, seu **método OnNotify** pode manipular eventos de várias maneiras. A tabela a seguir oferece sugestões sobre como manipular alguns dos eventos padrão. 
  
|**Tipo de evento**|**Manipulação em OnNotify**|
|:-----|:-----|
|Objeto movido  <br/> |Se o pai original do objeto movido estiver relacionado ao novo pai, atualize a exibição que começa com a pasta ou o contêiner do livro de endereços mais alto na hierarquia. Se os dois contêineres pai não estão relacionados, atualize ambos os seus visualizações.  <br/> |
|Nova mensagem  <br/> |Altere a interface do usuário para informar ao usuário sobre a chegada de uma ou mais mensagens novas. Coloque a pasta de recebimento no visualização atual.  <br/> |
|Erro  <br/> |Para todos os objetos, exceto a sessão, registre o erro se necessário e retorne. Para o objeto de sessão, faça logoff, se possível.  <br/> |
|Pesquisa concluída  <br/> |Nenhum processamento é necessário.  <br/> |
   
> [!NOTE]
> Manipuladores de notificação devem ser reentrantes. 
  

