---
title: Implementando uma tabela de One-Off contêiner
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
# <a name="implementing-a-container-one-off-table"></a>Implementando uma tabela de One-Off contêiner

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para acessar a tabela única pertencente a um de seus contêineres, o MAPI chama o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) do contêiner para abrir a propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) com a interface **IMAPITable.** Seu contêiner é solicitado a retornar sua tabela única quando um aplicativo cliente está tentando adicionar um destinatário ao contêiner. Se o contêiner permitir qualquer destinatário, o provedor poderá retornar sua própria implementação de tabela ou chamar [IMAPISupport::GetOneOffTable](imapisupport-getoneofftable.md) para retornar a implementação de MAPI. 
  
O conjunto de modelos na tabela única do contêiner deve refletir o tipo de destinatários que o contêiner específico pode conter. Normalmente, isso inclui um ou dois modelos, modelos para criar um usuário de mensagens individual ou uma lista de distribuição. Os identificadores de entrada para esses modelos são mantidos nas propriedades **PR_DEF_CREATE_MAILUSER** ([PidTagDefCreateMailuser](pidtagdefcreatemailuser-canonical-property.md)) e **PR_DEF_CREATE_DL** ([PidTagDefCreateDl](pidtagdefcreatedl-canonical-property.md)). No entanto, os contêineres não são limitados de forma alguma a esses tipos de entradas. Eles podem conter outros tipos de destinatários ou entradas que não são de destinatário, como diretórios. 
  

