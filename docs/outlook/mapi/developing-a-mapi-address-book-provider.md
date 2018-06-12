---
title: Desenvolvendo um provedor de catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 03f53dbfbe57db76ee8ceefda3f6938301f70da8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766400"
---
# <a name="developing-a-mapi-address-book-provider"></a>Desenvolvendo um provedor de catálogo de endereços MAPI

  
  
**Aplica-se a**: Outlook 
  
Um provedor de catálogo de endereços fornece informações de destinatário para aplicativos de cliente, para o repositório de mensagem e transporte provedores e MAPI. Informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres. Cada catálogo de endereços no perfil contribui um ou mais nível superior, ou pai, provedores de livro de contêineres ao catálogo de endereços MAPI, uma exibição integrada de informações de destinatário de todos os endereços em uma sessão. É por meio do catálogo de endereços MAPI que os clientes e outros provedores de serviços obtém acesso aos dados de um provedor de catálogo de endereços.
  
MAPI constrói o catálogo de endereços integrada por:
  
1. Recuperando os contêineres de nível superior de cada provedor de catálogo de endereços.
    
2. Recuperando a tabela de hierarquia do cada contêiner. 
    
3. Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada. É a tabela de hierarquia integrado que é exposta no cliente. 
    
MAPI impõe poucos requisitos de escritores de provedor de catálogo de endereços. A gama de recursos possíveis que você pode implementar como um gravador de catálogo de endereços é variados e flexíveis. Por exemplo, seu provedor poderia ser limitados fornecendo um modo de exibição somente leitura de um determinado tipo de informação de destinatário ou implementar um conjunto completo de recursos, talvez permitindo que os clientes ou provedores para tornar as inclusões ou modificações nos dados de destinatário e para impor critérios de pesquisa para a definição de exibições personalizadas. 
  
Dados do seu provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto. Alguns provedores de catálogo de endereços devem trabalhar com um sistema de mensagens específico, firmemente combinado com um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.
  
MAPI define um tipo especial de provedor de catálogo de endereços chamado um catálogo de endereços pessoal ou PAB, que implementa um único contêiner modificável e pode conter informações copiadas de outros contêineres, bem como as informações que criou diretamente do destinatário. Embora qualquer provedor de catálogo de endereços pode implementar um PAB e vários PABs podem ser adicionados a um perfil, apenas um desses provedores pode ser designado para operar como o PAB durante uma sessão de qualquer. 
  

