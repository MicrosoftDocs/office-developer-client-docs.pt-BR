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
ms.openlocfilehash: 2de51e1cf0f29c91e39eb3c6dbaab065fd7d5972
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590523"
---
# <a name="mapi-property-type-overview"></a>Visão geral do tipo de propriedade MAPI
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tipos de propriedade são constantes definidas pelo MAPI no MAPIDEFS. Arquivo de cabeçalho H que indicam o tipo de dados de um valor de propriedade. Todas as propriedades, se eles são definidos por MAPI, pelos aplicativos cliente ou por provedores de serviço, usam um desses tipos. 
  
Tipos de propriedade siga uma convenção de nomenclatura semelhante à usada para marcas de propriedade. Muitos tipos de propriedade tem uma versão de valor único e vários valores. Propriedades de valores única contenham um valor de seu tipo como um inteiro único ou uma cadeia de caracteres. A constante usada para representar uma propriedade de valor único tem duas partes: o prefixo PT_ e uma cadeia de caracteres que descreve o tipo real, como LONG ou STRING8. 
  
Propriedades de valores múltiplos contém mais de um valor de seu tipo. Ao contrário de matrizes de variante OLE, cada valor em uma propriedade de valores múltiplos é do mesmo tipo. A constante usada para representar vários valores de propriedades é criada, combinando o sinalizador MV_FLAG com a constante correspondente de valor único que representa o tipo de base. Existem três partes: o prefixo PT_ seguido MV_ seguido por uma cadeia de caracteres que descreve o tipo. Por exemplo, o tipo de uma propriedade que contenham inteiros vários é PT_MV_LONG e para várias cadeias de caracteres é PT_MV_STRING8.
  
A ilustração a seguir mostra a estrutura de uma estrutura de [SPropValue](spropvalue.md) para descrever um inteiro de valores múltiplos, uma propriedade do tipo PT_MV_LONG. O membro **Value** é expandido para incluir uma contagem do número de valores inteiros na propriedade e um ponteiro para uma matriz desses valores. 
  
**Multiple-value properties**
  
![Propriedades de valores múltiplos] (media/amapi_12.gif "Propriedades de valores múltiplos")
  
Embora o suporte para vários valores propriedades é opcional, MAPI recomenda clientes e provedores de serviços de suportem a ambos os tipos de propriedades porque fazendo afirmativo permite maior interação entre componentes compatível com MAPI.
  
A ilustração a seguir lista todas as constantes de tipo de propriedade diferentes, mostrando onde elas são armazenadas em uma estrutura **SPropValue** . O tamanho do membro **valor** depende do tipo específico. Observe que nem todos os tipos de valor único têm equivalentes de valores múltiplos. 
  
**Property type constants**
  
![Constantes de tipo de propriedade] (media/amapi_11.gif "Constantes de tipo de propriedade")
  
Trabalhando com uma propriedade de provedores de serviços e de clientes necessário seguir duas etapas:
  
1. Determine se a propriedade está disponível ou indisponível.
    
2. Se estiver disponível, recupere o valor da propriedade.
    
Em alguns casos, um provedor de cliente ou serviço só precisa verificar a existência de uma propriedade; outras vezes é necessário verificar se há um valor específico. Por exemplo, provedores de transporte tem três diferentes cursos de ação para processamento de **PR\_SEND_RICH_INFO** propriedade ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), um valor Boolean que indica se ou não uma mensagem deve ser transmitida com texto formatado. Se **PR\_SEND_RICH_INFO** é definido como TRUE, o provedor de transporte transmite o texto formatado. Se ele for definido como FALSE, o texto formatado é descartado antes da transmissão. Se **PR_SEND_RICH_INFO** não estiver disponível, o provedor de transporte segue seu curso padrão de ação, qualquer isto é para o provedor específico. 
  
MAPI define um tipo de propriedade especial, PT_UNSPECIFIED, que um provedor de cliente ou serviço pode usar para recuperar uma propriedade quando o tipo de propriedade é desconhecido. Para recuperar uma propriedade sem um conhecimento avançado de seu tipo, um provedor de cliente ou serviço chama um método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) e passa uma marca de propriedade formada pelo identificador da propriedade e o tipo de propriedade PT_UNSPECIFIED. **GetProps** retorna uma estrutura de [SPropValue](spropvalue.md) para a propriedade, substituindo PT_UNSPECIFIED com o tipo apropriado. Provedores de serviços de implementação **GetProps** são necessárias para dar suporte a PT_UNSPECIFIED. 
  
Alguns objetos MAPI suportam a propriedades que são os próprios objetos. Propriedades de objeto têm o tipo PT_OBJECT. Em vez de usar **IMAPIProp::GetProps** para acessar essas propriedades, os clientes e os provedores de serviço geralmente usuário ambos o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , especificando a interface adequada para o access ou um método no objeto dando suporte à propriedade. 
  
Porque acessando o valor da propriedade de um objeto envolve usando uma das interfaces do objeto, **GetProps** é inadequado. Com **GetProps**, o chamador acessa um valor de propriedade por meio de uma estrutura **SPropValue** . Com **IMAPIProp::OpenProperty**, o chamador recupera um ponteiro para uma interface que pode acessar o objeto. **OpenProperty** sempre pode ser usado para recuperar uma propriedade de objeto. Outra opção, chamando um método no objeto, não está disponível com a propriedade de cada objeto. 
  
Por exemplo, cada pasta dá suporte a duas tabelas, uma tabela de hierarquia e uma tabela de conteúdo. Nestas tabelas são propriedades da pasta; suas marcas de propriedade são **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) e **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). Tabelas são objetos que exigem a interface **IMAPITable** para acesso. Um cliente pode chamar o método de [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) da pasta para acessar a tabela de hierarquia, o método de [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) da pasta para acessar a tabela de conteúdo, ou a pasta [IMAPIProp::OpenProperty ](imapiprop-openproperty.md)método para acessar qualquer uma das tabelas. Para chamar **OpenProperty**, um cliente passa a marca de propriedade para a propriedade, como o primeiro parâmetro e um identificador de interface para a interface a ser usada para acesso como o segundo parâmetro. Esses parâmetros seria **PR_CONTAINER_HIERARCHY** ou **PR_CONTAINER_CONTENTS** e **IID_IMAPITable**.
  
Para obter uma lista completa dos tipos de valor único e vários valores de propriedade, consulte [Tipos de propriedade](property-types.md). 
  
## <a name="see-also"></a>Confira também

- [Visão geral da propriedade MAPI](mapi-property-overview.md)

