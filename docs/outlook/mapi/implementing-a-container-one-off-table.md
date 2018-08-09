---
title: Implementar a tabela única de um contêiner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 83351e18750ccbffbe60c4e19f9b04a9c94a42e2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767401"
---
# <a name="implementing-a-container-one-off-table"></a>Implementar a tabela única de um contêiner

  
  
**Aplica-se a**: Outlook 
  
Para acessar a tabela único pertencente a um dos seus contêineres, MAPI chama o método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com o **IMAPITable** interface. Seu contêiner é solicitado para retornar sua tabela único quando um aplicativo cliente está tentando adicionar um destinatário para o contêiner. Se o contêiner permite quaisquer destinatários, seu provedor pode retornar sua própria implementação de tabela ou chamada [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para retornar a implementação de MAPI. 
  
O conjunto de modelos na tabela únicos contêiner deve refletir o tipo de destinatários que pode conter no contêiner específico. Normalmente, isso inclui um ou dois modelos, modelos para a criação de um usuário individual de mensagens ou uma lista de distribuição. Os identificadores de entrada para esses modelos são mantidos no **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e propriedades de **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). No entanto, os contêineres a intenção não estão limitados a esses tipos de entradas. Eles podem conter outros tipos de destinatários ou entradas de não-recipient como diretórios. 
  

