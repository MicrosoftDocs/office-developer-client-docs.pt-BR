---
title: Implementar uma tabela de um contêiner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eabbde74-49a1-4eeb-a01d-67e45ae4b343
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 72dc73b6ed8519be2d8010544fdd5dc5b7b0f759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417417"
---
# <a name="implementing-a-container-one-off-table"></a>Implementar uma tabela de um contêiner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para acessar a tabela única pertencente a um dos seus contêineres, o MAPI chama o método [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com **** o IMAPITable interface. Seu contêiner é solicitado a retornar sua tabela única quando um aplicativo cliente está tentando adicionar um destinatário ao contêiner. Se o contêiner permitir qualquer destinatário, seu provedor poderá retornar sua própria implementação de tabela ou chamar [IMAPISupport:: GetOneOffTable](imapisupport-getoneofftable.md) para retornar a implementação MAPI. 
  
O conjunto de modelos na tabela de contêiner único deve refletir o tipo de destinatários que o contêiner específico pode conter. Normalmente, isso inclui um ou dois modelos, modelos para a criação de um usuário de mensagens individual ou uma lista de distribuição. Os identificadores de entrada desses modelos são mantidos nas propriedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). No enTanto, os contêineres não são por nenhum meio limitado a esses tipos de entradas. Eles podem conter outros tipos de destinatários ou entradas não-destinatários, como diretórios. 
  

