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
ms.openlocfilehash: b457fce208923ce01686812f20031e365842ccd8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593673"
---
# <a name="implementing-an-advise-sink-object"></a>Implementar um objeto de coletor de aviso

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um cliente pode implementar seus próprios objetos de coletor de eventos advise ou usar uma função do utilitário, [HrAllocAdviseSink](hrallocadvisesink.md). **HrAllocAdviseSink** cria um objeto de coletor de eventos advise com uma implementação do **OnNotify** que chama uma função de retorno de chamada. 
  
Há vantagens e desvantagens de usar **HrAllocAdviseSink**. Ele economiza seu trabalho, mas ela fornece nenhum controle sobre o objeto coletor de eventos advise que ele cria de contagem de referência. Portanto, os clientes que precisar controlar cuidadosamente o lançamento do coletor de eventos seus advise ou que tenham interdependência entre seu coletor de eventos advise e outro objeto do cliente devem construir sua própria implementação **IMAPIAdviseSink** e evitar o uso de ** HrAllocAdviseSink** todo. 
  
Um cliente implementando seu próprio coletor de eventos advise deve facilitam um objeto independente não relacionadas à ou dependentes quaisquer outros objetos de forma a eliminar possíveis complicações versão contando e o objeto de referência. No entanto, se você deve implementar seu coletor advise como parte de outro objeto ou incluir um ponteiro inverso para outro objeto como um membro de dados, é recomendável que as duas contagens de referência separada ser mantidas: um para o objeto referenciado pelo coletor de eventos advise e outro para o coletor de eventos de aviso. 
  
Quando a contagem de referência do objeto referenciado cai para zero, todos os seus métodos podem falhar e seu vtable pode ser destruído, mas a memória para o coletor de eventos advise deve permanecer intacta até após sua contagem de referência também cai para zero. Isso significa que o método de **lançamento** do coletor de eventos advise deve diminuir sua contagem de referência e término destruir o objeto quando essa contagem chegar a zero. Se não serão mantidas duas contagens de referência separada, seria fácil inadvertidamente destrua o coletor de eventos advise como parte do processo de **lançamento** do objeto abrangente. 
  
Clientes usando o **HrAllocAdviseSink** para implementar um coletor de advise devem ser igualmente cuidadosos para não incluir suas funções de retorno de chamada como um método no objeto de coletor de eventos do outro advise. Para clientes do C++, está tentando fazer isso e passe o ponteiro _this_ como um parâmetro. Essa é uma estratégia de perigosa porque os clientes geralmente liberem um objeto quando sua contagem de referência chega a zero. Liberar a memória para o objeto coletor de eventos de advise seria renderizar o ponteiro _this_ inválido. 
  
Dependendo do tipo de evento e a origem de advise, seu método **OnNotify** pode manipular eventos de diversas maneiras. A tabela a seguir oferece sugestões de como lidar com alguns dos eventos padrão. 
  
|**Tipo de evento**|**Tratamento de OnNotify**|
|:-----|:-----|
|Objeto movido  <br/> |Se o pai de original do objeto movido está relacionado ao novo pai, atualize o início do modo de exibição com a pasta ou o contêiner de catálogo de endereços mais alto na hierarquia. Se os contêineres dois pai não estão relacionados, atualize os dois de seus modos de exibição.  <br/> |
|Nova mensagem  <br/> |Altere a interface do usuário para informar ao usuário sobre a chegada de uma ou mais mensagens novas. Coloque a pasta de recebimento na exibição atual.  <br/> |
|Error  <br/> |Para todos os objetos, exceto a sessão, faça o erro, se necessário e retorno. Para o objeto de sessão, faça o logoff se possível.  <br/> |
|Pesquisa completa  <br/> |Nenhum processamento necessário.  <br/> |
   
> [!NOTE]
> Manipuladores de notificação devem ser reentrantes. 
  

