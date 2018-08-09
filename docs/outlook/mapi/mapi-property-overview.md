---
title: Visão geral da propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ed11677d09ae5acacced77373b2bca783d1ec0b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767924"
---
# <a name="mapi-property-overview"></a>Visão geral da propriedade MAPI

  
  
**Aplica-se a**: Outlook 
  
Uma propriedade é um atributo de um objeto MAPI. As propriedades descrevem algo sobre o objeto, como a linha de assunto de uma mensagem ou o tipo de endereço de um usuário de mensagens. MAPI define várias propriedades, algumas para descrever muitos objetos e alguns que são adequadas somente para um objeto de um determinado tipo. Clientes e provedores de serviços podem estender o conjunto do MAPI de propriedades predefinidas criando novas e propriedades personalizadas. Os clientes podem definir propriedades para descrever novas classes de mensagem, e provedores de serviços podem definir propriedades para expor recursos exclusivos de seu sistema de mensagens.
  
Propriedades podem ser persistente ou temporária. Propriedades que persistem a cada sessão podem ser armazenadas com os dados dos seus objetos ou no perfil. Propriedades temporárias existem apenas para a duração da sessão atual. 
  
Clientes e provedores de serviços podem mostrar propriedades aos usuários com uma tabela ou em uma folha de propriedades. Tabelas oferecem aos usuários uma exibição somente leitura de algumas das propriedades que pertencem a vários objetos. Os dados são exibidos em formato de linha e coluna, com cada linha representa um objeto e cada uma propriedade de coluna. Folhas de propriedades são caixas de diálogo com guias que exibem as propriedades relacionadas para um único objeto. Folhas de propriedades podem fornecer somente leitura ou acesso de leitura/gravação aos dados. Se um usuário tem permissão para fazer alterações é até o implementador da folha de propriedades.
  
A interface [IMAPIProp](imapipropiunknown.md) é o principal para trabalhar com propriedades. Todos os objetos que oferecem suporte a propriedades implementam **IMAPIProp**. **IMAPIProp** inclui métodos para recuperar valores de propriedade, copiando propriedades, as alterações e salvar essas alterações, o mapeamento entre os nomes de propriedade e seus identificadores e recuperar informações sobre um erro anterior. 
  
Existem diversas estruturas de dados para descrever propriedades e informações sobre propriedades. As estruturas usadas com mais frequência são o [SPropValue](spropvalue.md) e a estrutura de [SPropTagArray](sproptagarray.md) . A estrutura **SPropValue** contém as três partes das informações que descrevem uma propriedade: 
  
- Dados, ou o valor da propriedade.
    
- Tipo de dados do valor da propriedade, como um inteiro ou booleano. 
    
- Valor numérico dentro de um intervalo específico que identificam exclusivamente a propriedade e o componente responsável por manter a ele. Por exemplo, há um intervalo para armazenar o conteúdo de propriedades definidas pelo MAPI e outro intervalo para armazenar as propriedades de conteúdo da mensagem é definido por um cliente para uma classe de mensagem personalizada de mensagem. 
    
O tipo de propriedade e o identificador são combinados em um único componente chamado a marca de propriedade. As marcas de propriedade são constantes que podem ser usadas facilmente se referir à propriedade. Marcas de propriedade para propriedades definidas pelo MAPI são incluídas na MAPITAGS. Arquivo de cabeçalho H e no membro de uma estrutura de **SPropValue** **ulPropTag** . Provedores de serviços e clientes usam marcas de propriedade para identificar, recuperar e atualizar as propriedades correspondentes. 
  
A estrutura **SPropTagArray** é uma matriz contada das marcas de propriedade. Muitos dos métodos na **IMAPIProp** e outras interfaces usam uma estrutura de **SPropTagArray** para descrição das propriedades. 
  
## <a name="see-also"></a>Confira também



[Conceitos MAPI](mapi-concepts.md)

