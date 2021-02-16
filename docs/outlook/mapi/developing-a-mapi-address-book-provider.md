---
title: Desenvolvendo um provedor de lista de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409367"
---
# <a name="developing-a-mapi-address-book-provider"></a>Desenvolvendo um provedor de lista de endereços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de agendas fornece informações de destinatário para aplicativos cliente, para provedores de transporte e armazenamento de mensagens e para MAPI. As informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres. Cada livro de endereços no perfil contribui com um ou mais contêineres de nível superior, ou pai, para o livro de endereços MAPI, uma exibição integrada das informações de destinatário de todos os provedores de livro de endereços em uma sessão. É por meio do livro de endereços MAPI que os clientes e outros provedores de serviços têm acesso aos dados de um provedor de agendas.
  
MAPI builds the integrated address book by:
  
1. Recuperar os contêineres de nível superior de cada provedor de agendamento de endereços.
    
2. Recuperação da tabela de hierarquias de cada contêiner. 
    
3. Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada. É a tabela de hierarquia integrada exposta ao cliente. 
    
O MAPI impõe poucos requisitos para os autores de provedores de agendas. A variedade de recursos possíveis que você pode implementar como um autor de livro de endereços é variada e flexível. Por exemplo, seu provedor pode estar limitado a fornecer uma exibição somente leitura de um determinado tipo de informação de destinatário ou implementar um conjunto completo de recursos, talvez permitindo que clientes ou provedores façam adições ou modificações nos dados do destinatário e imponham critérios de pesquisa para definir exibições personalizadas. 
  
Os dados do provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto. Alguns provedores de agendamento de endereço devem trabalhar com um sistema de mensagens específico, fortemente unido a um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.
  
O MAPI define um tipo especial de provedor de livro de endereços chamado de um livro de endereços pessoal, ou PAB, que implementa um único contêiner modificável e pode manter informações de destinatário copiadas de outros contêineres, bem como informações criadas diretamente. Embora qualquer provedor de agendas possa implementar um PAB e vários PABs possam ser adicionados a um perfil, apenas um desses provedores pode ser designado para operar como PAB durante qualquer sessão. 
  

