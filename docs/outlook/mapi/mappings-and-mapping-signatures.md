---
title: Mapeamentos e Assinaturas de Mapeamento
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 773f6671-cc21-4d1f-a11d-308bc71c852d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cd26ce4bc2da3da639b4a611fc9a69f39b13e5f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410011"
---
# <a name="mappings-and-mapping-signatures"></a>Mapeamentos e Assinaturas de Mapeamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um provedor de serviços oferece suporte a propriedades nomeadas, cada conjunto de pares de identificador e nome é chamado de mapeamento. Os provedores de serviços podem dar suporte a um ou vários mapeamentos. Ou seja, um provedor de armazenamento de mensagens, por exemplo, pode implementar os métodos **GetIDsFromNames** e **GetNamesFromIDs** para todos os seus objetos de armazenamento de mensagens, pastas e mensagens para trabalhar com uma única lista de nomes e seus identificadores correspondentes. Outro provedor de armazenamento de mensagens pode ter uma lista para cada pasta e as mensagens contidas nele, ou implementar uma lista exclusiva para cada mensagem e cada pasta. Os provedores de armazenamento de mensagens que usam um mapeamento exclusivo para cada mensagem não devem permitir que propriedades nomeadas apareçam em suas tabelas de conteúdo de pasta porque, para um determinado nome de propriedade, o identificador de propriedade será diferente de mensagem para mensagem. MAPI recommends that providers keep it simple and operate with a single list for all of their objects including tables. 
  
Para cada mapeamento, os provedores de serviços devem fornecer uma assinatura de mapeamento. Uma assinatura de mapeamento é um valor binário, geralmente um GUID, que identifica exclusivamente um conjunto de identificadores de propriedade e seus nomes correspondentes. As assinaturas de mapeamento são armazenadas na propriedade **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. Os provedores de serviços devem alterar o valor de sua **propriedade PR_MAPPING_SIGNATURE** sempre que uma alteração for feita no mapeamento que ela representa. Por exemplo, **PR_MAPPING_SIGNATURE** deve ser atualizado se um novo identificador for atribuído a um nome ou um novo nome e par de identificadores for adicionado. 
  
Os clientes que trabalham com as propriedades nomeadas de objetos usam as propriedades PR_MAPPING_SIGNATURE **dos** objetos em operações de comparação e cópia. Para comparar identificadores de propriedade nomeados pertencentes a dois objetos, os clientes que não usam assinaturas de mapeamento devem chamar [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) em ambos os objetos para recuperar os nomes de cada um dos identificadores. Usar as assinaturas de mapeamento de objetos pode tornar essa chamada desnecessária. Quando dois objetos têm o mesmo valor para suas PR_MAPPING_SIGNATURE **propriedades,** eles usam o mesmo mapeamento. Os identificadores que usam o mesmo mapeamento podem ser comparados diretamente. Os provedores de serviços que implementam [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md) também podem tirar proveito da assinatura de mapeamento de um objeto. Ao copiar propriedades nomeadas entre objetos, os provedores de serviços podem evitar a etapa de conversão quando os objetos de origem e destino têm a mesma assinatura de mapeamento. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI denominada propriedades](mapi-named-properties.md)

