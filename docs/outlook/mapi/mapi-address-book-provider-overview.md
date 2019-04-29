---
title: Visão geral do provedor de catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426538"
---
# <a name="mapi-address-book-provider-overview"></a>Visão geral do provedor de catálogo de endereços MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de catálogo de endereços lidam com o acesso a informações de diretório. As informações de diretório consistem em dados de dois tipos de destinatários de mensagem: usuários de mensagens individuais e grupos de usuários de mensagens que normalmente são tratados juntos em listas de distribuição. Dependendo do tipo de destinatário e do provedor de catálogo de endereços, há uma ampla variedade de informações que podem ser disponibilizadas. Por exemplo, todos os provedores de catálogo de endereços armazenam o nome, o endereço e o tipo de endereço de um destinatário.
  
Cada provedor de catálogo de endereços organiza esses dados usando um ou mais contêineres. O número e a estrutura dos contêineres dependem da implementação do provedor do catálogo de endereços. Por exemplo, um provedor de catálogo de endereços pode usar um único contêiner para armazenar todas as informações, outra pode usar um contêiner de nível superior que contém sub-recipientes, e um terceiro pode usar vários contêineres de nível superior, cada um contendo sub-recipientes. Uma hierarquia de contêiner de catálogo de endereços pode ser muito profunda; Não há limite para o número de sub-recipientes que podem ser usados.
  
A ilustração a seguir mostra uma organização típica de catálogo de endereços MAPI.
  
**Address book organization**
  
![Organização do catálogo de endereços] (media/amapi_04.gif "Organização do catálogo de endereços")
  
O MAPI integra todas as informações fornecidas pelos provedores de catálogo de endereços instalados em um único catálogo de endereços, apresentando um modo de exibição unificado para o aplicativo cliente. A lista integrada mostra os contêineres de nível superior exibidos por cada um dos provedores de catálogo de endereços instalados. A maioria dos provedores de catálogos de endereços expõem apenas alguns contêineres (normalmente de um a três) no nível superior para inclusão no nível superior do catálogo de endereços integrado MAPI. Por exemplo, um provedor de catálogo de endereços pode tornar disponível "todos os usuários" e "usuários locais" como dois contêineres no nível superior.
  
Os usuários de aplicativos cliente podem exibir o conteúdo dos contêineres do catálogo de endereços e, em alguns casos, modificar o conteúdo. Os contêineres do catálogo de endereços podem ser criados com diferentes níveis de acesso, dependendo do provedor de catálogo de endereços. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

