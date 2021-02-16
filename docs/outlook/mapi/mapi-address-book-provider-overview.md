---
title: Visão geral do provedor de agenda de endereços MAPI
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
# <a name="mapi-address-book-provider-overview"></a>Visão geral do provedor de agenda de endereços MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de agendas lidam com o acesso às informações do diretório. As informações de diretório consistem em dados para dois tipos de destinatários de mensagens: usuários de mensagens individuais e grupos de usuários de mensagens que normalmente são abordados juntos em listas de distribuição. Dependendo do tipo de destinatário e do provedor do livro de endereços, há uma ampla variedade de informações que podem ser disponibilizadas. Por exemplo, todos os provedores de agendas armazenam o nome, o endereço e o tipo de endereço de um destinatário.
  
Cada provedor de agendas organiza esses dados usando um ou mais contêineres. O número e a estrutura dos contêineres dependem da implementação do provedor de agendas. Por exemplo, um provedor de livro de endereços pode usar um único contêiner para reter todas as informações, outro pode usar um contêiner de nível superior que contém subcontentores e um terceiro pode usar vários contêineres de nível superior, cada um mantendo subcontainers. Uma hierarquia de contêineres de um livro de endereços pode ser muito profunda; não há limite para o número de subcontainers que podem ser usados.
  
A ilustração a seguir mostra uma organização típica do livro de endereços MAPI.
  
**Address book organization**
  
![Organização do address book Address](media/amapi_04.gif "book")
  
MAPI integrates all the information supplied by the installed address book providers into a single address book, presenting a unified view to the client application. A lista integrada mostra os contêineres de nível superior exibidos por cada um dos provedores de agendas instalados. A maioria dos provedores de livro de endereços expõe apenas alguns contêineres (normalmente um a três) no nível superior para inclusão no nível superior do livro de endereços integrado MAPI. Por exemplo, um provedor de agendas pode disponibilizar "Todos os Usuários" e "Usuários Locais" como dois contêineres no nível superior.
  
Os usuários de aplicativos cliente podem exibir o conteúdo dos contêineres do livro de endereços e, em alguns casos, modificar o conteúdo. Os contêineres de agenda podem ser criados com níveis de acesso diferentes, dependendo do provedor de agendas. 
  
## <a name="see-also"></a>Confira também

- [Recursos e arquitetura MAPI](mapi-features-and-architecture.md)

