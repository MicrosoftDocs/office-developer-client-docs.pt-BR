---
title: Visão geral da propriedade MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 02e5b23f-1bdb-4fbf-a27d-e3301a359573
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 99887bab2b576e6e6c05414ee9daf1bd6e8d0463
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408324"
---
# <a name="mapi-property-overview"></a>Visão geral da propriedade MAPI

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Uma propriedade é um atributo de um objeto MAPI. As propriedades descrevem algo sobre o objeto, como a linha de assunto de uma mensagem ou o tipo de endereço de um usuário de mensagens. MAPI define muitas propriedades, algumas para descrever muitos objetos e algumas que são apropriadas apenas para um objeto de um tipo específico. Clientes e provedores de serviços podem estender o conjunto de propriedades predefinidos mapiados criando novas propriedades personalizadas. Os clientes podem definir propriedades para descrever novas classes de mensagens, e os provedores de serviços podem definir propriedades para expor os recursos exclusivos de seu sistema de mensagens.
  
As propriedades podem ser persistentes ou temporárias. Propriedades persistentes de sessão para sessão podem ser armazenadas com os dados de seus objetos ou no perfil. Existem propriedades temporárias apenas pela duração da sessão atual. 
  
Os clientes e provedores de serviços podem mostrar propriedades aos usuários com uma tabela ou uma folha de propriedades. As tabelas fornecem aos usuários uma exibição somente leitura de algumas das propriedades pertencentes a vários objetos. Os dados são exibidos no formato de linha e coluna, com cada linha representando um objeto e cada coluna de uma propriedade. Folhas de propriedades são caixas de diálogo com guias que exibem propriedades relacionadas para um único objeto. As folhas de propriedades podem fornecer acesso somente leitura ou leitura/gravação aos dados. Se um usuário tem permissão ou não para fazer alterações é de acordo com o implementador da folha de propriedades.
  
A interface [IMAPIProp](imapipropiunknown.md) é a interface principal para trabalhar com propriedades. Todos os objetos que suportam propriedades **implementam IMAPIProp**. **IMAPIProp** inclui métodos para recuperar valores de propriedade, copiar propriedades, fazer alterações e salvar essas alterações, mapeamento entre nomes de propriedade e seus identificadores e recuperar informações sobre um erro anterior. 
  
Há várias estruturas de dados para descrever propriedades e informações sobre propriedades. As estruturas mais comumente usadas são a [estrutura SPropValue](spropvalue.md) e a [estrutura SPropTagArray.](sproptagarray.md) A **estrutura SPropValue** contém as três informações que descrevem uma propriedade: 
  
- Dados, ou valor, da propriedade.
    
- Tipo de dados do valor da propriedade, como inteiro ou booleano. 
    
- Valor numérico dentro de um intervalo específico que identifica exclusivamente a propriedade e o componente responsável por mantê-lo. Por exemplo, há um intervalo para manter propriedades de conteúdo de mensagens definidas por MAPI e outro intervalo para manter propriedades de conteúdo de mensagens definidas por um cliente para uma classe de mensagem personalizada. 
    
O tipo de propriedade e o identificador são combinados em um único componente chamado marca de propriedade. Marcas de propriedade são constantes que podem ser usadas para se referir facilmente à propriedade. Marcas de propriedade para propriedades definidas por MAPI estão incluídas em MAPITAGS. Arquivo de header H e no **membro ulPropTag** de uma **estrutura SPropValue.** Os clientes e provedores de serviços usam marcas de propriedade para identificar, recuperar e atualizar as propriedades correspondentes. 
  
A **estrutura SPropTagArray** é uma matriz contada de marcas de propriedade. Muitos dos métodos em **IMAPIProp** e outras interfaces usam uma estrutura **SPropTagArray** para descrever propriedades. 
  
## <a name="see-also"></a>Confira também



[Conceitos de MAPI](mapi-concepts.md)

