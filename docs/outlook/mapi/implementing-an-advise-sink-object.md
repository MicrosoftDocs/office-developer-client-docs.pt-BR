---
title: Implementar um objeto de coletor de aviso
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7461c4f6-7030-4ba2-ada4-26ebfbbfa001
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ecaad65d28f74b843b86ca82dab9a833ade77363
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351097"
---
# <a name="implementing-an-advise-sink-object"></a>Implementar um objeto de coletor de aviso

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode implementar seus próprios objetos de coletor de aviso ou usar uma função de utilitário, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** cria um objeto de coletor de aviso com uma **** implementação de OnNotify que invoca uma função de retorno de chamada. 
  
Há vantagens e desvantagens de usar o **HrAllocAdviseSink**. Ele pode economizar trabalho, mas não fornece controle sobre a referência de contagem do objeto de coletor de aviso que ele cria. Portanto, os clientes que precisam controlar cuidadosamente sua versão do coletor de aviso ou que têm interdependências entre o seu coletor de aviso e outro objeto de cliente devem criar sua própria implementação de **IMAPIAdviseSink** e evitar usar ** HrAllocAdviseSink** completamente. 
  
Um cliente que esteja implementando seu próprio coletor de avisos deve torná-lo um objeto independente não relacionado ao ou depender de outros objetos, para eliminar possíveis complicações na contagem de referência e no lançamento do objeto. No enTanto, se você deve implementar o seu coletor de aviso como parte de outro objeto ou incluir um ponteiro de retorno para outro objeto como um membro de dados, é recomendável que duas contagens de referência separadas sejam mantidas: uma para o objeto referenciado pelo coletor de aviso e outra para o coletor de aviso. 
  
Quando a contagem de referência do objeto referenciado cai para zero, todos os seus métodos podem falhar e sua vtable pode ser destruída, mas a memória do coletor de avisos deve permanecer intacta até que a contagem de referência também seja igual a zero. Isso significa que o método **Release** do coletor de avisos deve decrementar sua contagem de referência e concluir a destruição do objeto quando essa contagem chega a zero. Se duas contagens de referência separadas não forem mantidas, será fácil destruir inadvertidamente o coletor de aviso como parte do processo de **lançamento** do objeto de abrangeção. 
  
Os clientes que usam o **HrAllocAdviseSink** para implementar um coletor de aviso devem ser igualmente cuidados de não incluir a função de retorno de chamada como um método em outro objeto de coletor de aviso. Para clientes C++, é tentador fazer isso e passar o ponteiro como __ um parâmetro. Essa é uma estratégia perigosa porque os clientes normalmente liberam um objeto quando sua contagem de referência chega a zero. Liberar a memória do objeto de coletor de aviso renderizaria o __ ponteiro inválido. 
  
Dependendo do tipo de evento e da fonte de aviso, o método **OnNotify** pode manipular eventos de várias maneiras. A tabela a seguir oferece sugestões sobre como lidar com alguns dos eventos padrão. 
  
|**Tipo de evento**|**Lidando com onNotify**|
|:-----|:-----|
|Objeto movido  <br/> |Se o pai original do objeto movido estiver relacionado ao novo pai, atualize o modo de exibição começando com o contêiner de pasta ou catálogo de endereços mais alto na hierarquia. Se os dois contêineres pai não estiverem relacionados, atualize os dois modos de exibição.  <br/> |
|Nova mensagem  <br/> |Altere a interface do usuário para informar ao usuário sobre a chegada de uma ou mais mensagens novas. Coloque a pasta receber no modo de exibição atual.  <br/> |
|Error  <br/> |Para todos os objetos, exceto a sessão, registre o erro se necessário e retornar. Para o objeto Session, faça logoff, se possível.  <br/> |
|Pesquisa concluída  <br/> |Nenhum processamento necessário.  <br/> |
   
> [!NOTE]
> Manipuladores de notificação devem ser reentrante. 
  

