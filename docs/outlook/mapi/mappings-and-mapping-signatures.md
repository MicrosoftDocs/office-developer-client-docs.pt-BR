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
ms.openlocfilehash: b5c8fd8c757de995e2a2e4239be614cf171fcb44
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566184"
---
# <a name="mappings-and-mapping-signatures"></a>Mapeamentos e assinaturas de mapeamento

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Quando um provedor de serviços oferece suporte a propriedades nomeadas, cada conjunto de pares de identificador e nome é conhecido como um mapeamento. Provedores de serviços podem oferecer suporte para mapeamento de uma ou várias. Que é, um provedor de armazenamento de mensagens, por exemplo, pode implementar os métodos **GetIDsFromNames** e **GetNamesFromIDs** para todas as suas mensagens, pasta e objetos de repositório de mensagem para trabalhar com uma única lista de nomes e seus identificadores correspondentes. Outro provedor de repositório de mensagem pode ter uma lista para cada pasta e as mensagens contidas dentro dele ou implementar uma lista exclusiva para cada mensagem e cada pasta. Provedores de armazenamento de mensagem que usam um mapeamento exclusivo para cada mensagem não devem permitir propriedades nomeadas apareça em suas tabelas de conteúdo de pasta porque um nome de propriedade fornecida, o identificador da propriedade será diferente de mensagem a mensagem. MAPI recomenda provedores mantê-lo simples e operam com uma única lista de todos os seus objetos incluindo tabelas. 
  
Para cada mapeamento, provedores de serviço devem fornecer uma assinatura de mapeamento. Uma assinatura de mapeamento é um valor binário, geralmente um GUID, que identifica exclusivamente um conjunto de identificadores de propriedade e seus nomes correspondentes. Assinaturas de mapeamento são armazenadas na propriedade de **PR_MAPPING_SIGNATURE** ([PidTagMappingSignature](pidtagmappingsignature-canonical-property.md)) de um objeto. Provedores de serviços devem alterar o valor de sua propriedade **PR_MAPPING_SIGNATURE** sempre que uma alteração é feita para o mapeamento que ele representa. Por exemplo, **PR_MAPPING_SIGNATURE** deve ser atualizado se um novo identificador é atribuído a um nome ou um novo nome e o par de identificador é adicionado. 
  
Como trabalhar com as propriedades nomeadas dos objetos de clientes usam propriedades **PR_MAPPING_SIGNATURE** dos objetos nas operações de comparação e cópia. Para comparar denominado identificadores que pertencem aos dois objetos, os clientes que não usam assinaturas de mapeamento devem chamar [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) em ambos os objetos para recuperar os nomes para cada um dos identificadores de propriedade. Usar as assinaturas de mapeamento de objetos, essa chamada pode renderizar desnecessárias. Quando dois objetos têm o mesmo valor para suas propriedades **PR_MAPPING_SIGNATURE** , eles usam o mesmo mapeamento. Identificadores que usam o mesmo mapeamento podem ser comparados diretamente. Provedores de serviços que implementam [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps](imapiprop-copyprops.md) também podem aproveitar o de assinatura de mapeamento de um objeto. Quando a cópia denominado propriedades entre objetos, provedores de serviços podem evitar a etapa de conversão quando os objetos de origem e destino têm a mesma assinatura de mapeamento. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)


[MAPI denominada propriedades](mapi-named-properties.md)

