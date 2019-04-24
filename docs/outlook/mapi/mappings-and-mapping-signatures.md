---
title: Mapeamentos e assinaturas de mapeamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357635"
---
# <a name="mappings-and-mapping-signatures"></a>Mapeamentos e assinaturas de mapeamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um provedor de serviços dá suporte a propriedades nomeadas, cada conjunto de pares identificador e nome é chamado de mapeamento. Os provedores de serviços podem suportar um ou vários mapeamentos. Ou seja, um provedor de repositório de mensagens, por exemplo, pode implementar os métodos **GetIDsFromNames** e **GetNamesFromIDs** para todos os seus objetos Message, Folder e Message Store para trabalhar com uma única lista de nomes e seus identificadores correspondentes. Outro provedor de repositório de mensagens pode ter uma lista para cada pasta e as mensagens contida nela, ou implementar uma lista exclusiva para cada mensagem e cada pasta. Os provedores de repositórios de mensagens que usam um mapeamento exclusivo para cada mensagem não devem permitir que as propriedades nomeadas apareçam nas tabelas de conteúdo da pasta porque, para um determinado nome de propriedade, o identificador de propriedade será diferente da mensagem para a mensagem. A MAPI recomenda que os provedores mantenham a simplicidade e operem com uma única lista de todos os seus objetos, incluindo as tabelas. 
  
Para cada mapeamento, os provedores de serviços devem fornecer uma assinatura de mapeamento. Uma assinatura de mapeamento é um valor binário, geralmente um GUID, que identifica exclusivamente um conjunto de identificadores de propriedade e seus nomes correspondentes. As assinaturas de mapeamento são armazenadas na propriedade **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. Os provedores de serviços devem alterar o valor para a propriedade **PR_MAPPING_SIGNATURE** sempre que uma alteração é feita no mapeamento que representa. Por exemplo, **PR_MAPPING_SIGNATURE** deve ser atualizado se um novo identificador for atribuído a um nome ou um novo nome e par de identificadores for adicionado. 
  
Os clientes que trabalham com as propriedades nomeadas de objetos usam as propriedades **PR_MAPPING_SIGNATURE** de objetos nas operações de comparação e cópia. Para comparar identificadores de propriedade nomeados pertencentes a dois objetos, os clientes que não usam assinaturas de mapeamento devem chamar [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md) em ambos os objetos para recuperar os nomes de cada um dos identificadores. O uso de assinaturas de mapeamento de objetos pode renderizar essa chamada desnecessária. Quando dois objetos têm o mesmo valor para suas propriedades **PR_MAPPING_SIGNATURE** , eles usam o mesmo mapeamento. Os identificadores que usam o mesmo mapeamento podem ser comparados diretamente. Os provedores de serviços que implementam o [IMAPIProp:: CopyTo](imapiprop-copyto.md) e [IMAPIProp:: CopyProps](imapiprop-copyprops.md) também podem aproveitar a assinatura de mapeamento de um objeto. Ao copiar propriedades nomeadas entre objetos, os provedores de serviços podem evitar a etapa de conversão quando os objetos de origem e de destino têm a mesma assinatura de mapeamento. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI denominada propriedades](mapi-named-properties.md)

