---
title: Visão geral de provedor de catálogo de endereços MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 855b145bcca8007601eb8e841665306d4c58982f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576558"
---
# <a name="mapi-address-book-provider-overview"></a>Visão geral de provedor de catálogo de endereços MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
No catálogo de endereços provedores alça acesso às informações de diretório. Informações sobre o diretório dados consiste de dois tipos de destinatários da mensagem: individuais de usuários e grupos de usuários de mensagens que são geralmente resolvidos juntos em listas de distribuição de mensagens. Dependendo do tipo de destinatário e o provedor de catálogo de endereços, há uma ampla gama de informações que podem ser disponibilizadas. Por exemplo, todos os provedores de catálogo de endereços armazenam o nome, endereço e tipo de endereço do destinatário.
  
Cada provedor de catálogo de endereços organiza esses dados usando um ou mais contêineres. O número e a estrutura dos contêineres depende da implementação do provedor de catálogo de endereços. Por exemplo, um provedor de catálogo de endereços pode usar um único recipiente para armazenar todas as informações de outro pode utilizar um contêiner de nível superior que armazena subcontêineres e um terceiro pode usar vários contêineres de nível superior, cada subcontêineres fornecerá. Uma hierarquia de contêiner de catálogo de endereços pode ser bastante profunda; Não há nenhum limite no número de subcontêineres que podem ser usados.
  
A ilustração a seguir mostra uma organização típica de catálogo de endereços MAPI.
  
**Address book organization**
  
![Organização de catálogo de endereços] (media/amapi_04.gif "Organização de catálogo de endereços")
  
MAPI integra todas as informações fornecidas pelos provedores de catálogo de endereços instalada em um único catálogo de endereços, apresentando uma exibição unificada para o aplicativo cliente. A lista integrada mostra os contêineres de nível superior indicados por cada um dos provedores de catálogo de endereços instalada. A maioria dos provedores de catálogo de endereços expor somente alguns contêineres (normalmente um a três) no nível superior para inclusão em um nível superior do catálogo de endereços integrado do MAPI. Por exemplo, um fornecedor de catálogo de endereços pode tornar "disponível todos os usuários" e "Local" como dois contêineres de nível superior.
  
Os usuários de aplicativos cliente podem exibir o conteúdo dos contêineres do catálogo de endereços e, em alguns casos, modificar o conteúdo. Contêineres de catálogo de endereços podem ser criados com os níveis de acesso diferente, dependendo do provedor de catálogo de endereços. 
  
## <a name="see-also"></a>Confira também

- [Arquitetura e os recursos MAPI](mapi-features-and-architecture.md)

