---
title: Visão geral do tipo de propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b762f5fb-7c2c-4303-96f7-0b6e657146c9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 58dd25f09b76d97fd6441915225756a19f4ec3cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438194"
---
# <a name="mapi-property-type-overview"></a>Visão geral do tipo de propriedade MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tipos de propriedade são constantes definidas por MAPI em MAPIDEFS. Arquivo de header H que indica o tipo de dados subjacente de um valor de propriedade. Todas as propriedades, sejam elas definidas por MAPI, por aplicativos cliente ou por provedores de serviços, use um desses tipos. 
  
Os tipos de propriedade seguem uma convenção de nomenlagem semelhante à usada para marcas de propriedade. Muitos tipos de propriedade têm uma versão de valor único e de vários valores. Propriedades de valor único contêm um valor de seu tipo, como um único inteiro ou cadeia de caracteres. A constante usada para representar uma única propriedade de valor tem duas partes: o prefixo PT_ e uma cadeia de caracteres que descreve o tipo real, como LONG ou STRING8. 
  
Propriedades de vários valores contêm mais de um valor de seu tipo. Ao contrário de matrizes variantes OLE, cada valor em uma propriedade de múltiplos valores é do mesmo tipo. A constante usada para representar propriedades de múltiplos valores é criada combinando o sinalizador MV_FLAG com a constante de valor único correspondente que representa o tipo base. Há três partes: o prefixo PT_ seguido por MV_ seguido por uma cadeia de caracteres que descreve o tipo. Por exemplo, o tipo de uma propriedade que contém vários inteiros é PT_MV_LONG e para várias cadeias de caracteres é PT_MV_STRING8.
  
A ilustração a seguir mostra a estrutura [de uma estrutura SPropValue](spropvalue.md) para descrever um inteiro de vários valores, uma propriedade do tipo PT_MV_LONG. O **membro** Value é expandido para incluir uma contagem do número de valores inteiros na propriedade e um ponteiro para uma matriz desses valores. 
  
**Multiple-value properties**
  
![Propriedades de vários valores](media/amapi_12.gif "Propriedades de vários valores")
  
Embora o suporte para propriedades de vários valores seja opcional, o MAPI recomenda que os clientes e provedores de serviços suportem ambos os tipos de propriedades porque isso permite maior interação entre componentes compatíveis com MAPI.
  
A ilustração a seguir lista todas as diferentes constantes de tipo de propriedade, mostrando onde elas estão armazenadas em uma **estrutura SPropValue.** O tamanho do membro **Value** depende do tipo específico. Observe que nem todos os tipos de valor único têm equivalentes de vários valores. 
  
**Property type constants**
  
![Constantes de tipo de propriedade](media/amapi_11.gif "Constantes de tipo de propriedade")
  
Clientes e provedores de serviços que trabalham com uma propriedade precisam seguir duas etapas:
  
1. Determine se a propriedade está disponível ou indisponível.
    
2. Se disponível, recupere o valor da propriedade.
    
Às vezes, um cliente ou provedor de serviços precisa apenas verificar a existência de uma propriedade; outras vezes, é necessário verificar se há um valor específico. Por exemplo, provedores de transporte têm três cursos de ação diferentes para processar a propriedade **PR \_ SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), um valor Boolean que indica se uma mensagem deve ou não ser transmitida com texto formatado. Se **a \_ SEND_RICH_INFO** PR estiver definida como TRUE, o provedor de transporte transmitirá o texto formatado. Se for definido como FALSE, o texto formatado será descartado antes da transmissão. Se **PR_SEND_RICH_INFO** não estiver disponível, o provedor de transporte seguirá seu curso de ação padrão, seja qual for o caso para o provedor específico. 
  
MAPI define um tipo de propriedade especial, PT_UNSPECIFIED, que um cliente ou provedor de serviços pode usar para recuperar uma propriedade quando o tipo de propriedade é desconhecido. Para recuperar uma propriedade sem conhecimento antecipado de seu tipo, um cliente ou provedor de serviços chama o método [IMAPIProp::GetProps](imapiprop-getprops.md) de um objeto e passa uma marca de propriedade com o identificador da propriedade e o tipo de propriedade PT_UNSPECIFIED. **GetProps** retorna uma [estrutura SPropValue](spropvalue.md) para a propriedade, substituindo PT_UNSPECIFIED pelo tipo apropriado. Os provedores de serviços que **implementam GetProps** são necessários para dar suporte PT_UNSPECIFIED. 
  
Alguns objetos MAPI suportam propriedades que são objetos por conta própria. As propriedades do objeto têm o tipo PT_OBJECT. Em vez de usar **IMAPIProp::GetProps** para acessar essas propriedades, os clientes e provedores de serviços geralmente usam o método [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) especificando a interface apropriada para acesso ou um método no objeto que dá suporte à propriedade. 
  
Como acessar o valor de uma propriedade de objeto envolve o uso de uma das interfaces para o objeto, **GetProps** é inadequado. Com **GetProps**, o chamador acessa o valor de uma propriedade por meio de **uma estrutura SPropValue.** Com **IMAPIProp::OpenProperty**, o chamador recupera um ponteiro para uma interface que pode acessar o objeto. **OpenProperty** sempre pode ser usado para recuperar uma propriedade de objeto. A outra opção, chamando um método no objeto, não está disponível com todas as propriedades de objeto. 
  
Por exemplo, cada pasta oferece suporte a duas tabelas, uma tabela de hierarquia e uma tabela de conteúdo. Essas tabelas são propriedades da pasta; suas marcas de propriedade **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) e **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Tabelas são objetos que exigem a interface **IMAPITable** para acesso. Um cliente pode chamar o método [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta para acessar a tabela de hierarquia, o método [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para acessar a tabela de conteúdo ou o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) da pasta para acessar qualquer uma das tabelas. Para chamar **OpenProperty**, um cliente passa a marca de propriedade da propriedade como o primeiro parâmetro e um identificador de interface para a interface a ser usada para acesso como o segundo parâmetro. Esses parâmetros seriam **PR_CONTAINER_HIERARCHY** ou **PR_CONTAINER_CONTENTS** e **IID_IMAPITable**.
  
Para uma lista completa dos tipos de propriedade de valor único e de vários valores, consulte [Tipos de propriedade.](property-types.md) 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

