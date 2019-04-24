---
title: Desenvolver um provedor de catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 821cc42d-eebb-4327-b2d4-594421a5c22c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 1db3ce53a1da60d946e52a03369c10547676277f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316699"
---
# <a name="developing-a-mapi-address-book-provider"></a>Desenvolver um provedor de catálogo de endereços MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Um provedor de catálogo de endereços fornece informações de destinatários para aplicativos clientes, para provedores de transporte e armazenamento de mensagens e para MAPI. As informações do destinatário são organizadas hierarquicamente em compartimentos de armazenamento conhecidos como contêineres. Cada catálogo de endereços no perfil contribui para um ou mais recipientes de nível superior ou pai para o catálogo de endereços MAPI, uma visão integrada das informações de destinatário de todos os provedores de catálogo de endereços em uma sessão. É através do catálogo de endereços MAPI que os clientes e outros provedores de serviços obtêm acesso aos dados de um provedor de catálogo de endereços.
  
MAPI cria o catálogo de endereços integrados por:
  
1. Recuperar os contêineres de nível superior de cada provedor de catálogo de endereços.
    
2. Recuperar a tabela de hierarquia de cada contêiner. 
    
3. Copiando cada tabela de hierarquia em uma tabela de hierarquia integrada. É a tabela de hierarquia integrada que é exposta ao cliente. 
    
O MAPI impõe alguns requisitos nos escritores do provedor de catálogo de endereços. O intervalo de possíveis recursos que você pode implementar como gravador de catálogo de endereços é variado e flexível. Por exemplo, o provedor pode ser limitado ao fornecimento de um modo de exibição somente leitura de um tipo específico de informações do destinatário ou implementar um conjunto completo de recursos, talvez permitindo que clientes ou provedores façam inclusões ou modificações nos dados do destinatário e imponham critérios de pesquisa para definição de modos de exibição personalizados. 
  
Os dados do provedor podem residir localmente em um arquivo ou banco de dados ou em um servidor remoto. Alguns provedores de catálogos de endereços servem para trabalhar com um sistema de mensagens específico, intimamente acoplado a um provedor de transporte, enquanto outros podem operar com qualquer sistema de mensagens.
  
O MAPI define um tipo especial de provedor de catálogo de endereços chamado de catálogo de endereços pessoal, ou PAB, que implementa um único contêiner modificável e pode conter informações de destinatário copiadas de outros contêineres, bem como informações criadas diretamente. Embora qualquer provedor de catálogo de endereços possa implementar um PAB e vários PABs possam ser adicionados a um perfil, somente um desses provedores pode ser designado para operar como o PAB durante uma única sessão. 
  

